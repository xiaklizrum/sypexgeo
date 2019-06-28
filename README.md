Lightweight, dependency-less SypexGeo module
============================
Differences with [base module](https://github.com/JiSoft/yii2-sypexgeo):
------------
- Remove [yiisoft/yii2](https://github.com/yiisoft/yii2) dependency
- Remove [SxGeoCityMax.dat](https://github.com/JiSoft/yii2-sypexgeo/blob/master/SxGeoCityMax.dat) database (12.9 MB)
- PSR-2 format

Installation
------------

```
composer require xiaklizrum/sypexgeo
```

Usage
-----
Example:
```php
<?php
    use SypexGeo\SxGeo;
    $pathOfYouDbFile = './SxGeoCityMax.dat';
    $geo = new SxGeo($pathOfYouDbFile);
    var_dump($geo->getCityFull('188.93.132.196'));
?>
```
Output:
```html
array (size=3)
  'city' => 
    array (size=5)
      'id' => int 2022890
      'lat' => float 48.48272
      'lon' => float 135.08379
      'name_ru' => string 'Хабаровск' (length=18)
      'name_en' => string 'Khabarovsk' (length=10)
  'region' => 
    array (size=4)
      'id' => int 2022888
      'name_ru' => string 'Хабаровский край' (length=31)
      'name_en' => string 'Khabarovskiy Kray' (length=17)
      'iso' => string 'RU-KHA' (length=6)
  'country' => 
    array (size=6)
      'id' => int 185
      'iso' => string 'RU' (length=2)
      'lat' => int 60
      'lon' => int 100
      'name_ru' => string 'Россия' (length=12)
      'name_en' => string 'Russia' (length=6)
```