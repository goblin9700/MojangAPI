# MojangAPI
##### PHP class to use official Mojang API

## Installation

You only need to download this file: [mojang-api.class.php](https://github.com/MineTheCube/MojangAPI/blob/master/mojang-api.class.php)

## Usage

See an usage of this class in [`example.php`](https://github.com/MineTheCube/MojangAPI/blob/master/example.php) file.
To see all methods available, see the MojangAPI interface: [`mojang-api.interface.php`](https://github.com/MineTheCube/MojangAPI/blob/master/mojang-api.interface.php) (not needed in your project).

## Example

```php
// Require API
require 'mojang-api.class.php';

// Get UUID from username
$uuid = MojangAPI::getUuid('MTC');
echo 'UUID: <b>' . $uuid . '</b><br>';

// Get his name history
$history = MojangAPI::getNameHistory($uuid);
echo 'First username: <b>' . reset($history)['name'] . '</b><br>';

// Print player's head
$img = '<img src="' . MojangAPI::embedImage(MojangAPI::getPlayerHead($uuid)) . '" alt="Head of MTC">';
echo 'Skin:<br>' . $img;
```

## Result

![Preview](http://i.imgur.com/0HV8thN.jpg)
