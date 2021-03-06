# yii2-ueditor

# Requirements

- PHP >= 5.4.0
- Composer
- Yii2

# Installation

``` sh
composer require eddycjy/yii2-ueditor "@dev"
```

# Configuration

## Use File

Add to configs file 

- yii-basic : config/web.php 

- yii-advanced: common/config/main.php

``` php
'modules' => [
    'ueditor' => [
         'class' => 'Ueditor\UeditorModule',
    ],
],

```

or change ue-configs, upload folder root_path **@app/web**

``` php
'modules' => [
    'ueditor' => [
         'class' => 'Ueditor\UeditorModule',
         'imageUrlPrefix' => '',
         'imagePathFormat' => '/upload/image/{yyyy}{mm}{dd}/{time}{rand:6}',
         'scrawlUrlPrefix' => '',
         'scrawlPathFormat' => '',
         'snapscreenUrlPrefix' => '',
         'snapscreenPathFormat' => '',
         'catcherUrlPrefix' => '',
         'catcherPathFormat' => '',
         'videoUrlPrefix' => '',
         'videoPathFormat' => '',
         'fileUrlPrefix' => '',
         'filePathFormat' => '',
         'imageManagerUrlPrefix' => '',
         'imageManagerListPath' => '',
         'fileManagerUrlPrefix' => '',
         'fileManagerListPath' => '',
    ],
],
```



# Usage

Config view/form

``` php
<?= $form->field($model, 'content')->widget(\Ueditor\Widgets\Ueditor::className()) ?>
```

or widget

``` php
<?= \Ueditor\Widgets\Ueditor::widget([]) ?>
```

or config advanced ueditor reference [Docs](http://fex.baidu.com/ueditor/#start-config)

``` php
<?= \Ueditor\Widgets\Ueditor::widget([
    'id' => 'content',
    'options' => [
        'initialFrameWidth' => 666,
    ],
]) ?>
```

# License

MIT