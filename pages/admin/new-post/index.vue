<template>
    <div class="admin-new-post-page">
        <section class="new-post-form">
            <form @submit.prevent="onSave">
                <AppControlInput v-model="editedPost.author">Nombre Author</AppControlInput>
                <AppControlInput v-model="editedPost.title">Titulo</AppControlInput>
                <AppControlInput v-model="editedPost.thumbnailLink">Link de imagen pequeña</AppControlInput>
                <AppControlInput
                    control-type="textarea"
                    v-model="editedPost.content">
                    Content</AppControlInput>
                <AppButton type="submit">Save</AppButton>
                <AppButton
                    type="button"
                    style="margin-left: 10px"
                    btn-style="cancel"
                    @click="onCancel">Cancel</AppButton>
            </form>
        </section>
    </div>
</template>

<script>
import AppControlInput from '~/components/UI/AppControlInput'
import AppButton from '~/components/UI/AppButton'
export default {
    components : {
        AppControlInput,
        AppButton
    },
    data () {
        return {
            editedPost:{
                author: '',
                title: '',
                thumbnailLink: '',
                content: '',
            }
        }
    },
    methods :{
        onSave: function(){            
            console.log(this.editedPost)
        },
        onCancel (){            
            this.$router.push('/admin')            
        }
    }    
}
</script>