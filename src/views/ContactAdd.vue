<template>
    <div v-if="contact" class="page">
        <h4>Add contact</h4>
        <ContactForm :contact="contact" @submit:contact="onAddContact" />
        <p>{{ message }}</p>
    </div>

</template>
<script>
import ContactForm from '@/components/ContactForm.vue';
import { contactService } from '@/services/contact.service';
export default {
    components: {
        ContactForm,
    },
    data() {
        return {
            contact: {},
            message: '',
        };
    },
    methods: {
        async onAddContact(contact) {
            try {
                await contactService.create(contact);
                this.message = 'Add contact successfully';
            } catch (error) {
                console.log(error);
            }
        },
    },
    created() {
        this.message = '';
    },
};
</script>