## SHUEI AI Blogging

This repository contains the source code and blog posts for the Shuei AI Team blog, powered by Jekyll.

## Creating a New Post

To create a new blog post, follow these steps:

1. Navigate to the `_posts/` directory in your local repository.

2. Create a new file named in the format `YYYY-MM-DD-post-title.md`, where `YYYY-MM-DD` is the publication date and `post-title` is the title of your post.

3. At the top of the file, add the following front matter:

   ```yaml
   ---
   layout: post
   title: "Post Title"
   date: YYYY-MM-DD HH:MM:SS +0000
   author: Your Name
   categories: [category1, category2]
   ---
   ```

   Replace the placeholders with the appropriate values for your post.

4. Write your post's content below the front matter, using Markdown syntax.

5. Save the file and commit your changes to the repository.

## Local Deployment

To preview your blog posts locally, follow these steps:

1. Install Jekyll and its dependencies by running:

   ```bash
   bundle install
   ```

2. Start the Jekyll development server with:

   ```bash
   bundle exec jekyll serve
   ```

3. Open your web browser and navigate to `http://localhost:4000`. You should see your blog with the latest posts.

4. As you make changes to your posts or the site configuration, Jekyll will automatically rebuild the site and refresh your browser.

## Contributing

If you find any issues or have suggestions for improving the blog, feel free to open an issue or submit a pull request on the repository's GitHub page.

## License

This blog is licensed under the [MIT License](LICENSE).
