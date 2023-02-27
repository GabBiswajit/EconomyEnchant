# General

EconomyEnchant Shop For Pocketmine 4.0.0, With Many features

## Commands

Commands | Default
--- | ---
`/eshop` | True

## Feature
* Support Multiple Economys
* Support Multiple CustomEnchant
* Support EnchantTable Direct
* Support Sound When Enchant Success
* Auto Check Enchant Available in Hand
* Blacklist System
* Customable Message
* Customable Form (GUI / UI)
* Form
  - Configurable Form
  - Slide for Level
* GUI
  - Configurable GUI
  - If the enchant exceeds 26 Will be Divided into Pages
  - Confirmation GUI

## How to Registering Enchantment
Do you want to register your enchant Into this EnchantShop, Please follow this [Wiki](https://github.com/XanderID/EconomyEnchant/wiki/Registering-Enchantment)

## API
First Import Class XanderID\EconomyEnchant\Manager\EnchantManager</br>
- Getting Item Flags
  * EnchantManager::getItemFlags(/** Items you want */);
- Checking if Enchant Blacklisted
  * EnchantManager::isEnchantBlacklisted(/** Name the enchantment with Lower */);
- Checking if Enchant blacklisted in Item
  * EnchantManager::isItemBlacklisted(/** The Item */, /** Name Enchantment with Lower */);

## Screenshot
* Form ( UI )
  - Selecting Form
    ![Screenshot](https://github.com/XanderID/EconomyEnchant/blob/main/.screenshot/Form1.jpg)
  - Confirmation Form
    ![Screenshot](https://github.com/XanderID/EconomyEnchant/blob/main/.screenshot/Form2.jpg)
* InvMenu ( GUI )
  - Selecting GUI ( Page )
    ![Screenshot](https://github.com/XanderID/EconomyEnchant/blob/main/.screenshot/GUI1.jpg)
  - Confirmation GUI
    ![Screenshot](https://github.com/XanderID/EconomyEnchant/blob/main/.screenshot/GUI2.jpg)

## Supported Custom Enchant Plugin
* [PiggyCustomEnchants](https://poggit.pmmp.io/p/PiggyCustomEnchants) by DaPigGuy
* [VanillaEC](https://poggit.pmmp.io/p/VanillaEC/) By David-pm-pl

## Supported Economy Providers

* [EconomyAPI](https://poggit.pmmp.io/p/EconomyAPI) by onebone/poggit-orphanage
* [BedrockEconomy](https://poggit.pmmp.io/p/BedrockEconomy) by cooldogedev
* [Capital](https://poggit.pmmp.io/p/Capital/) By SOF3
* [XP](https://github.com/pmmp/PocketMine-MP) By PocketMine-MP

# Config

``` YAML

---
# Please don't edit this, only for internal use
config-version: 2

# Your Economy plugin name
# Available: BedrockEconomy, EconomyAPI, Capital, XP, Auto
# If you select auto but there is no Economy Plugin it will automatically use XP
economy: "Auto"

# Selector for Capital Economys
selector: []

# Can EnchantTable Redirect to EconomyEnchant
enchant-table: true

# Add Anvil Sound to Player if Enchant is Successful
sound: true

# Form Type
# Can use UI or GUI
form-type: "UI"

# Form
form:
 # Buy Menu
 buy-shop:
  # Title for BuyShop
  title: "EnchantShop"
  # Content for BuyShop
  content: "Select Enchantment:"
  # Tag: {price} Price Enchantment, {enchant} Name Of Enchantment
  button:
   # Only can 0-1
   0: "{enchant}"
   1: "{price}"
 # Submit Menu
 submit:
  # Title for SubmitMenu
  title: "EnchantShop"
  # Content
  # Tag: {price} Price of Enchantment
  content: "§aYou will pay {price} Per Level"
  # Max Content
  max-content: "§aYour item has reached the level limit!"
  # Slider Content
  slider: "Level"

# GUI
gui:
 # Buy Menu
 buy-shop:
  # Title for BuyShop
  title: "EnchantShop"
  # Tag: {level} Level Enchantment, {enchant} Name Of Enchantment
  name: "§f{enchant} §b{level}"
  # Tag: {price} Price Enchantment
  # if you want to empty lore just put value []
  lore:
   - "Price for This Enchant {price}"
 # Submit Menu
 submit:
  # Title for SubmitMenu
  title: "EnchantShop"
  # Buy Item
  buy:
   # Buy Item Name
   # Tag: {level} Level Enchantment, {enchant} Name Of Enchantment
   name: "Buy §f{enchant} §b{level}"
   # Buy Item Lore
   # Tag: {price} Price Enchantment
   # if you want to empty lore just put value []
   lore:
    - "Are you sure to buy"
    - "This Enchant With price {price}"
   # Cancel Item
  cancel:
   # Cancel Item Name
   name: "§cCancel"
   # Cancel Item Lore
   # if you want to empty lore just put value []
   lore:
    - "Cancel buying Enchantment"

# Message
message:
 # Cannot Enchant On This Item
 err-item: "§cYou cannot add Enchantment to This Item!"
 # Exit Message
 exit: "§aThank you for visiting!"
 # Successfully Buy Enchant
 # Tag: {enchant} Name Enchantment, {item} Name Item, {price} Price Enchantment
 success: "§aSuccessfully Enchant {enchant} to {item}, with Price {price}"
 # Error Max Enchant
 max: "§cEnchant failed!, Your item is reached Max Level"
 # Error Money not Enough
 # Tag: {need} Needed Money
 enough: "§cYour money is not enough need {need}"

# Mode
# If false Enchantment those that are not set will not be in the shop
# If true Enchantment Auto added and price will be to Default ( Not Setted )
mode: true

# Enchantment
enchantment:
 # Name Enchantment
 sharpness:
  # Price
  price: 1000
 # Default, If the enchantment is not set above
 # it will be redirected here
 default:
  # Price
  price: 10000
  
# Blacklist Enchantment from Shop
# if you want blacklist just add
# example: ["sharpness", "silk_touch"] or ["sharpness"]
blacklist: []

# Blacklist Enchantment from Item
# if you want blacklist just add
# example: 
# blacklist:
#  sharpness: ["diamond_sword"]
# If you want add meta just item_name:meta
blacklist-item: []
...

```

# Additional Notes

- If you find bugs or want to give suggestions, please visit [here](https://github.com/XanderID/EconomyEnchant/issues)
