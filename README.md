# ZF2 Js Appender

This ZF2 Module aims to provide a fast way to configure Javascript libraries.

## Rationale

Often happens to have to set up a Javascript library and many times it would be nice to have a place where you can configure them
and perhaps with the ability to override the configuration rather than throw them in the view.


## Examples

### Google Analytics

**In your configuration**

```php
return array(
    'zf2_js_appender' => array(
        'ga' => array(
            'type'   => 'google-analytics',
            'values' => array(
                'monitoring_id' => 'UA-XXXXXXXX-X',
                'domain'        => 'yourdomain.com'
            ),
        )

    ),
);
```

**In your template**

```php
<?php echo $this->jsAppender('ga');?>
```