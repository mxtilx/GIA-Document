# Auto collector Assist

- Note: After v0.6.1, Auto Collector wan changed from Flow to Mission.

## Introduction

Auto Collector Assist can automatically acquire most of the materials in Teyvat World such as gatherables, loot, etc.

Example: Automatic collect sweet flowers, automatic kill Silme.

This function intergrates Auto Combat Assist, Auto Move Assist, Auto Pickup Assist. Make sure you have read the information about them before using.

## Function Introduction

- Specify the collection, GIA will select the cloest collection from the database and start-up.
- Can collect resource/enemy
- Automatic continuous collect
- Revive at the State when somebody died.

## Quick Start

Set the paramaters at the Collector.json.

Start the Auto Collector from the GUI.

## Parameters Setting

- Recommanded editing in the GUI

| key             | item                                                                                           |
| --------------- | ---------------------------------------------------------------------------------------------- |
| collection_name | 需要采集的物品名称                                                                             |
| collection_type | type of collection，devided into `COLLECTION`（general collection）and `ENEMY`（combat drops） |

## Collector Log

Coollector Log(collection_log.json) is the log file generated by Auto Collector, including:

| key         | item                                    |
| ----------- | --------------------------------------- |
| time        | 采集时间                                |
| id          | 采集物id                                |
| error_code  | 退出原因                                |
| picked item | All items collected during that collect |

## Collection Selection Priority

When there are multiple locations of the collection, the weights are calculated accroding to the historical collection success rate and distance of collection.

## Collected Locations

Collected location including the id of collected items. Automatic generated.

## Blacklist Settings

Add the id to the list of corresponding items to block these collection items.

If the collection of some ids often fails, you can add them to the blacklist and they will be automatic skipped in subsequent collection.
