# esx_accessories

Shops with accessories (hat/helmet, glasses, masks, ears accessories). You can put on or take off the accessories with a menu. Accessories saved in database.

/!\ Works only with accessories purchased in the special areas of the clothing store, not via the esx_clotheshop script.

## Requirements
* Dependencies For Full Functionality
  * [esx_skin](https://github.com/esx-framework/esx-legacy/tree/main/%5Besx%5D/esx_skin)
  * [esx_datastore](https://github.com/esx-framework/esx-legacy/tree/main/%5Besx_addons%5D/esx_datastore)

## Download

### Using Git
- Clone repository from github
- Move all dependencies and esx_accessories to you resource folder

```
cd Downloads
git clone https://github.com/esx-framework/esx-legacy.git
```

### Using Release
- Download https://github.com/esx-framework/esx-legacy/archive/refs/tags/1.7.5.zip
- Move all dependencies and esx_accessories to you resource folder

## Installation
- Import `esx_accessories.sql` in your database
- Add this to your `server.cfg`:

```
ensure esx_accessories
```

## Commands

```
/accessory
```