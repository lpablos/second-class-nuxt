<template>
    <div class="admin-page">
        <section class="new-post">
            <AppButton  @click="$router.push('/admin/new-post')">Crear Posts</AppButton>            
        </section>
        <section class="existing-posts">
            <h1>Posts Existentes Admin</h1>
            <PostsList isAdmin />

        </section>
    </div>
</template>
<script>
import PostsList from '~/components/posts/PostsList'
import AppButton from '~/components/UI/AppButton'

export default {
    components : {
        PostsList,
        AppButton
    },
    layout:'admin'
}
</script>

<style scoped>

    .admin-page{
        padding: 20px;
    }

    .new-post{
        text-align: center;
        border-bottom: 2px solid #ccc;
        padding-bottom: 10px;
    }

    .existing-posts h1 {
        text-align: center;
    }
   
</style>