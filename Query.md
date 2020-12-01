# Query

| Property | Value           |
| -------- | --------------- |
| order    | 'ASC' \| 'DESC' |
| orderby  | 'none' \|       |



## Example 1

```php
<?php

  $post = array(
    'post_type' => 'post-name',
    'posts_per_page' => 1 | 2 | any number,
    'post_status' =>  'publish | pending | draft | auto-draft | future | private | inherit | trash | any',
    'orderby' => $order_by,
    'order'   => $order,
    'paged' => 1 | 2 | any number
  );

  $query = new WP_Query($post);
    while($query -> have_posts() ):
?>
    
  // HTML ....
    
<?php endwhile; wp_reset_postdata(); ?>
```



