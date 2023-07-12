# Datto Item Vault
Welcome to the **DIV**, or Datto Item Vault, where all items deleted in Vault Cleanings go.

# What even is this?
***In case you stumbled across this repository and don't understand what it's about***

This repository is essentially about the online looter-shooter video game Destiny 2, by Bungie. In Destiny, you can collect many items such as weapons and armor, but you have limited space on each of your characters (of which you can create three) to store those items. That's where the in-game Vault system comes in. You can store any excess items in there.

There is, of course, a limit to the amount of items you can store in your Vault. This limit has been increased by Bungie over the years, mostly at the request of the playerbase, since Destiny 2 launched in 2017. As of the creation of this repository, the limit is 600 items. Another important point to mention is that the Vault is shared across all your characters.

To those of you who don't play Destiny 2, you may be wondering why it's even necessary to have such a large limit to Vault space. You can only use so many weapons and armor at a time, or even keep them on your characters. Well, every once in a while, we Destiny players like to switch things up, so we keep the stuff we're not _currently_ using in the Vault until we decide we want to use them... or until a new update to the game makes a certain weapon or piece of armor much better than it previously was.

So, now that you understand the Vault system in Destiny, it's time to explain who is Datto and what are Vault Cleanings.

## Datto and the Vault Cleanings
[Youtuber](https://www.youtube.com/@DattoDoesDestiny) and [Twitch Streamer](https://www.twitch.tv/datto) Datto is the biggest content creator in the Destiny community, and not just in numbers. Let's put it this way: look up how many years the Destiny franchise has existed for, then add 1 to that. That's how many years Datto has been covering Destiny in his Youtube channel.

Datto is also of the opinion that nobody should need more Vault space than Bungie has already given us. This opinion is all well and good, especially because most players aren't getting good enough loot to justify keeping it in your Vault. But, content creators play the game _a lot_, and get _a lot_ of good items as a result. Some have it worse than others, but many of them seem to almost reach the limit of their Vaults.

Here's the problem: every year, Bungie releases a new expansion to the game, which all Destiny players know will bring more items, meaning more loot to collect... and put in your Vault. Maybe it's just about putting the old stuff in there and using the new items, or maybe it's about preferring the old items you were already comfortable with. Either way, items are going to end up in your Vault.

When Bungie was about to release the Witch Queen expansion for Destiny 2 in 2022, it became a popular trend among Destiny content creators to ask Datto for help to clean their Vaults ahead of the new expansion... since he didn't think they needed all that Vault space anyway. Datto, being friends with many of them, obliged. The result: hours upon hours of Datto asking content creators why they were keeping outdated, duplicate, unnecessary or otherwise bad items in their Vaults.

## Sunset items
Now, I mentioned outdated items, which begs an explanation for those who are either new to Destiny or haven't played it at all. A few years into Destiny 2, Bungie noticed that many players weren't using the new items that came with every season, and that certain weapons still dominated the inventories of players even when they were years old. Bungie determined that, with every season, only the items released in the past year of Destiny would still be able to be updated to the new level cap by players. This was called Sunsetting... and it didn't last very long. It was a very unpopular decision among players, and soon Bungie backtracked and no more items were sunset.

At that point, however, a lot of items had already gone through the sunsetting proccess, and they stayed that way. This is why we have "outdated" items in Destiny.

# Work in Progress
There have been many vault cleanings, and they are all recorded in extremely long videos. It also takes a lot of time to manually input all of the data into the spreadsheet. If you're reading this, that means the data available will be updated as soon as I am able to do it.

# Regarding the data
I am trying to collect as much information as possible on all deleted items, which sometimes means information that is not shown in the videos, such as the first two perks of a weapon roll, or a weapon's masterwork (when it is not masterworked). That means the data will be, in many parts, incomplete. However, I stil think there can be some useful insights by recording all of this in a dataset for future analysis.

In the meantime, you can find descriptions of each column below:

## creator_name (string)
Contains the name of the content creator doing the Vault Cleaning with Datto.

## video_link (string)
Link to the Youtube video of the Vault Cleaning.

## item (string)
Name of the deleted item.

## rarity (string)
Indicates the item's rarity level. In Destiny, the rarity of an item can be Common, Uncommon, Rare, Legendary, or Exotic.

## type (string)
Indicates what kind of item it is, usually Weapon or Armor.

## class (string)
Indicates which kind of item it is within its type. For Armor, indicates which character class it belongs to. This name was chosen because it is very likely that Bungie utilized OOP to identify common attributes and functions of certain Weapon types.

## slot (string)
Which character slot the item belongs to. For Weapons, can be either Kinetic, Energy or Power. For Armor, Helmet, Gauntlets, Chest Armor, Legs or Class Item.

## season (int-64)
Indicates which Destiny 2 season this item is attributed to. This is determined by what icon appears on the weapon in the videos.

## sunset (bool)
Indicates whether the item is sunset or not.

## masterworked (bool)
Indicates whether the item has been masterworked or not. If an Armor piece is masterworked, all of its attributes (stats) will be increased by 2.

## masterwork_trait (string)
Only non-null in case the item is a Weapon. Indicates which weapon attribute (stats) is the masterwork on that weapon. If the previous column holds a value of `True`, this attribute is increased by 10. This value is automatically added to the stats of a Weapon.

## craftable (bool)
Only non-null in case the item is a Weapon. Indicates whether a Weapon can be crafted or not.

## crafted (bool)
Only non-null in case the item is a Weapon. Indicates whether this particular instance of the Weapon has been crafted or not.

## pinnacle/ritual (bool)
Only non-null in case the item is a Weapon. Indicates whether this Weapon was the Pinnacle or Ritual Weapon of a particular season or not.

## element (string)
Indicates the damage type of the Weapon, or elemental affinity of the Armor piece (for Destiny's old armor system). NaN if the damage type is Kinetic.

## intrinsic (string)
Only non-null in case of Exotic items. Contains name of the main Exotic perk.

## exotic_catalyst (string)
Only non-null in case of Exotic Weapons. Contains name of the Exotic Catalyst perk, in case it is activated in the weapon.

## frame (string)
Only non-null in case of non-Exotic Weapons. Contains the designated Weapon frame, which usually indicates recoil patterns, impact and RPM on the Weapons.

## perk_1 (string)
Only non-null in case the item is a Weapon. Contains the name of the selected perk in the first perk column of a Weapon at the moment of deletion. May be NaN if this is not shown in the video.

## perk_2 (string)
Only non-null in case the item is a Weapon. Contains the name of the selected perk in the second perk column of a Weapon at the moment of deletion. May be NaN if this is not shown in the video.

## perk_3 (string)
Only non-null in case the item is a Weapon. Contains the name of the selected perk in the third perk column of a Weapon at the moment of deletion.

## perk_4 (string)
Only non-null in case the item is a Weapon. Contains the name of the selected perk in the fourth perk column of a Weapon at the moment of deletion.

## origin_trait (string)
Contains the name of the item's origin trait. Origin traits were only introduced in season 16 with the Witch Queen expansion, therefore items from previous seasons generally do not have origin traits. However, some weapons from seasons prior to The Witch Queen gained reprised versions with origin traits, but the icon that indicates which season that weapon instance was incorporated into the game _did not change_.

## Weapon Stats (int-64)
The next columns will contain the attributes of weapons. I won't pretend to know what each stat means, since I'm only vaguely aware of what a few of them do. For example, Range has to do with the damage fall-off of a weapon, and Aim Assistance has to do with bullet magnetism. I'm sure there are YouTube videos and articles explaining each one of these stats in depth, but I haven't gone looking.

### Impact
Applies to most weapons, with the exception of GLs (grenade launchers) and rocket launchers.

### Range
Applies to most weapons, with the exception of GLs, rockets, combat bows and swords.

### Stability
Applies to most weapons, with the exception of glaives and swords.

### Handling
Applies to most weapons, with the exception of swords.

### Reload Speed
Applies to most weapons, with the exception of swords.

### Aim Assistance
Applies to most weapons, with the excpetion of swords.

### Zoom
Applies to most weapons, with the exception of swords.

### Airborne Effectiveness
Applies to most weapons, with the exception of swords.

### Recoil Direction
Applies to most weapons, with the exception of swords.

### RPM
Applies to most weapons, with the exception of bows, fusion rifles, linear fusion rifles and swords.

### Magazine
Applies to most weapons, with the exception of swords.

### Accuracy and Draw Time
Apply only to bows. Draw Time is measured in miliseconds (ms).

### Charge Time
Applies only to fusion rifles and linear fusion rifles. Measured in miliseconds (ms).

### Shield Duration
Applies only to glaives.

### Blast Radius and Velocity
Apply only to GLs and rockets.

### Swing Speed, Charge Rate, Guard Resistance, Guard Efficiency, Guard Endurance and Ammo Capacity
Apply only to swords.

## Armor Stats (int-64)
The last columns contain the attributes of armor pieces. Each of these stats influence the character's own stats when the armor is equipped.

### Mobility
Influences character movement. For Hunters, influences class ability recharge rate.

### Resilience
Influences character damage resistance. For Titans, influences class ability recharge rate.

### Recovery
Influences character health regeneration. For Warlocks, influences class ability recharge rate.

### Discipline
Influences grenade ability recharge rate.

### Intellect
Influences super ability recharge rate.

### Strength
Influences melee ability recharge rate.

### total_stat_roll
Sum of all armor stats. On occasion, this will include the value of any armor mods that can increase the value of an armor stat.

# Regarding the analysis
My analysis will only begin once I finish the dataset, which will take a long time, as I mentioned above. Nonetheless, if you want to use the partial data for your own analysis, feel free to do so! I encourage anyone willing to use this dataset. If you find any errors, you can contact me through my email to let me know.
