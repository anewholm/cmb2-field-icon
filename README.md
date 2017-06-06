# CMB2 Field Icon

# Usage
  array(
    'id' => $prefix . 'location_metabox_icon',
    'title' => __( 'Icon', $plugin_slug ),
    'object_types' => array( $post_type, ), // Post type
    'context' => 'side',
    'priority' => 'high',
    'show_names' => false,
    'fields' => array(        
      array(
        'name' => __( 'Icon', $plugin_slug ),
        'id' => $plugin_slug . '_location_icon',
        'type' => 'icon',
        'desc' => 'Used in Maps.',
        'options' => array(
          'paths' => array( 
            THIS_PLUGIN_PATH . 'public/assets/images',
            wp_upload_dir()['path'], // Since 2.0.0
            'http://www.flaticon.com/packs/holiday-travelling-3',
          ),
        ),
      ),
    ),      
  );
