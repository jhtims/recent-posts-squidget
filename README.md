# recent-posts-squidget
A Blog Posts widget for WordPress that shows a certain number of recent posts.

<h4>From the Blog</h4>	
                <?php query_posts('posts_per_page=1'); ?> <!-- Change the number to show a certain # of posts -->
                    <?php while ( have_posts() ) : the_post(); ?> <!-- The Loop -->
                        <!-- loop content here --> 
                        <h2><?php the_title(); ?></h2>
                        <?php the_excerpt(); ?> 
                        <a class="read-more-link" href="<?php the_permalink(); ?>">Read More <span>&rsaquo;</span></a>
                        <!-- end -->
                    <?php endwhile; ?> <!-- Loop Ends -->
                <?php wp_reset_query(); ?>
              
/* Recent Blog Posts Example CSS */              
.blog-post {
	width: 50%;
}
.blog-post h4 {
	font-size: 16px;
	font-family: 'Montserrat';
	color: #a6a6a6;
	text-transform: uppercase;
}
.blog-post h2 {
	font-size: 24px;
	font-family: 'Montserrat';
	font-weight: bold;
}
.blog-post .read-more-link {
	font-size: 24px;
	font-family: 'Montserrat';
	font-weight: bold;
	color: #45ac9d;
	text-transform: uppercase;
}

Customize query
<? php query_posts('cat=8&posts_per_page=5&author=123'); ?>
- Category: Get by ID #
- Posts per Page: Get by number of recent posts you want to see
- Author: Get by ID #
