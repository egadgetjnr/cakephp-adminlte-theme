# CakePHP AdminLTE Theme

## Installation

You can install using [composer](http://getcomposer.org).

    composer require maiconpinto/cakephp-adminlte-theme

### Enable Plugin

```php
// config/bootstrap.php

Plugin::load('AdminLTE', ['bootstrap' => true, 'routes' => true]);
```

### Enable theme

```php
// src/Controller/AppController.php

public function beforeRender(Event $event)
{
	$this->viewBuilder()->theme('AdminLTE');
}
```

### Enable Form

```php
// src/View/AppView.php

public function initialize()
{
    $this->loadHelper('Form', ['className' => 'AdminLTE.Form']);
}
```

### Configure

```php
// src/Controller/AppController.php

public function beforeRender(Event $event)
{
    // ...
    $this->set('theme', Configure::read('Theme'));
}
```

```php
// To customize configuration paste it at end of file config/bootstrap.php

Configure::write('Theme', [
    'title' => 'AdminLTE',
    'logo' => [
        'mini' => '<b>A</b>LT',
        'large' => '<b>Admin</b>LTE'
    ]
]);
```

### Customize Layout

Replace the files according to the image.

![Dashboard](docs/dashboard.png)

1. `src/Template/Element/nav-top.ctp`
2. `src/Template/Element/aside-main-sidebar.ctp`
3. `src/Template/Element/aside/user-panel.ctp`
4. `src/Template/Element/aside/form.ctp`
5. `src/Template/Element/aside/sidebar-menu.ctp`
6. `src/Template/Element/aside-control-sidebar.ctp`
7. `src/Template/Element/footer.ctp`

### Wiki

[FormHelper](https://github.com/maiconpinto/cakephp-adminlte-theme/wiki/FormHelper)

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
