<template>
    <div class="blog-post">
        <div class="topic-image">
            <img :src="blogs[0].image" alt="topic-image">
        </div>
        <div class="blog-post-content">
            <div class="user-info">
                <div class="avatar"><img :src="require('@/assets/images/avatar/default.svg')" alt="avatar"></div>
                <p style="font-size: 14px;">Addmin<br/>Mar 13 - 1 min</p>
            </div>
            <div class="topic-title"><router-link to="/about">Silky Sands, Turquoise Surf</router-link></div>
            <div class="topic-content"><p>Create a blog post subtitle that summarizes your post in a few short, punchy sentences and entices your audience to continue reading. Welcome to your blog post. Use this space to connect with your readers and potential customers in a way that’s current and interesting. Think of it as an ongoing conversation where you can share updates about business, trends, news, and more. “Do you have a design in mind for your blog? Whether you prefer a trendy postcard look or you’re going for a more editorial style blog - there’s a stunning layout for everyone.” You’ll be posting loads of engaging content, so be sure to keep your blog organized with Categories that also allow visitors to explore more of what interests them. Create Relevant Content Writing a blog is a great way to position yourself as an authority in your field and captivate your readers’ attention. Do you want to improve your site’s SEO ranking? Consider topics that focus on relevant keywords and relate back to your website or business. You can also add hashtags (#vacation #dream #summer) throughout your posts to reach more people, and help visitors search for relevant content. Blogging gives your site a voice, so let your business’ personality shine through. Choose a great image to feature in your post or add a video for extra engagement. Are you ready to get started? Simply create a new post now.</p></div>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      blogs: [
        {
          image: require('@/assets/images/blogs/travel-1.png')
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import '@/assets/scss/_variable.scss';
.blog-post {
    width: 100%;
    height: auto;
    padding: 20px 0;
    text-align: left;

    .topic-image {
        width: 100%;
        min-height: 200px;
        height: 400px;
        img {
            height: 100%;
            object-fit: cover;
        }
    }

    &-content {
        width: 100%;
        height: auto;
        padding: 20px;

        .topic-title {
            padding: 10px 0;
            font-size: 24px;
            color: black;
            &:hover{
                color: $blue-text;
                cursor: pointer;
            }
            a {
                color: inherit;
                text-decoration: none;
            }
        }

        .topic-content {
            margin-bottom: 10px;
            border-bottom: 1px solid gray;
            p {
                font-size: 18px;
                white-space: nowrap;
                overflow: hidden;
                text-overflow: ellipsis;
                max-width: 100%;
            }
        }

        .user-info {
            height: 40px;
            width: 100%;
            display: flex;
            .avatar {
                width: 40px;
                height: 40px;
                margin-right: 8px;
                img {
                    width: 100%;
                }
            }
        }
    }
}
@media screen and (max-width: 480px) {
    .blog-post {
        .topic-image {
            height: 200px;
        }
    }
}
</style>
