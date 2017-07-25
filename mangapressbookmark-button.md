{% method %}
## mangapress_bookmark_button($attrs)

Bookmark button template tag. Adds a bookmark button for users to mark where they've left off while browsing.

### Parameters
* `$attrs (array)` Array of parameters.
    * `$show_history (boolean)` Show bookmark history link and drop-down. Defaults to false.
    * `$echo (boolean)` Specify whether or not to display or return output. Defaults to true (display output).

{% sample lang="php" -%}
### Example
Short example of using `mangapress_bookmark_button()`:
```php
<div class="container">
    <?php if (have_posts()): ?> 

        <div class="hfeed">
        <?php while (have_posts()): the_post() : ?>

            <div <?php post_class(); ?>>
                <?php mangapress_comic_navigation($args); ?>
                <?php 
                // display bookmark button and history drop-down
                mangapress_bookmark_button(array('show_history' => true)); ?>

                <h2><?php the_title(); ?></h2>

                <div class="entry-content">
                    <?php the_post_thumbnail(); ?>
                </div>
            </div>            

        <?php endwhile; ?> 
        </div>

    <?php endif; ?>    
</div>
```

{% endmethod %}

