{% method %}
## mangapress_end_latest_comic()
Ends a Latest Comic loop. See [mangapress_start_latest_comic()](/mangapress-start-latest-comic.md)

### Parameters
None

### Usage
{% sample lang="php" -%}
```php
<?php    
    mangapress_start_latest_comic();

    if (have_posts()) :
        while (have_posts()) : the_post(); ?>

        <!-- loop markup -->

        <?php endwhile;
    endif;

    mangapress_end_latest_comic();
?>
```

{% endmethod %}
