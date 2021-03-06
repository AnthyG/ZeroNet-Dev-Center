## Introduction

Before we start creating zites, it is useful to know how zites work on ZeroNet. This tutorial will take you through how to create an empty zite, where to put your code, what you need before you can publish your zite, and how they are updated, transfered, and kept secure.

Zites are made up of basic web code, including html, css, and js. However, json files are used for storing data and for telling ZeroNet what databases you have and how they are structured.

Since ZeroNet makes no use of a server - everything is downloaded to your computer and ran locally - there is no way to do server side scripting. However, this is remedied by using the ZeroNet API called ZeroFrame. This API lets you ...[^1]

## Creating A Zite

There are currently two ways of creating a zite. You can clone an existing zite, or you can create your own zite from scratch. If you decide to clone a zite, there are many of them you can choose from, including ... However, if you wan't to create your own zite from scratch, that is what the next few tutorials are going to cover.

In order to clone a zite, find a zite you want to clone, visit the zite so that it is downloaded to your computer. Next, go back to ZeroHello and find the zite in the sidebar. Click the menu icon, and press 'Clone'.

## The Sidebar

The Sidebar is _the_ place, where you can view information about any zite. It can be accessed by visiting a zite, and pulling the transluscent circle with the `0` in the middle, to the left. Here you can see an interactive globe that you can rotate, which displays all the peers over the globe.
There is a list of different items under it:
1. **Peers**:
Shows to how many peers you are connected, how many there are to which you can connect, how many use Onion, and the total amount of peers
2. **Data Transfer**: Shows how much data you have sent and received on the zite opened
3. **Files**: Shows what the summed size of the different file-formats are
4. **Size Limit**: Shows, how much of the filesize-limit you are using (in %), what the available free space is, on your harddrive, and an input to set the zites filesize-limit
5. **Optional Files**: Shows how much data you have downloaded, of all the optional files on the zite
6. **Download and help distribute all files**: Switch, to toggle if you want to download and seed _all_ the optional files
7. **Database**: Shows how big the database is, the path to it (relative to the zites path), a button to reload the Database-Scheme, and a button to rebuild the database
8. **Identity Address**: Shows how much storage you filled on the zite, of which the total is set by the Owner, and your Authentication-Address, with a button to select another account
9. **Site Control**: The first button tries to fetch the newest version available to any connected peer, the second pauses the download of any new data, and the third deletes the complete zite from the harddrive
10. **Site Address**: Displays the zites address (this might be helpful for finding the zite in your data-dir, if you are accessing it via a `.bit`-address)
11. **Missing Files**: Shows a list of all files, that are missing, according to the ZeroNet-Client
12. **This is my site**: Switch, to toggle, if you own this zite. If this is active, a few other items will appear underneath

The List-part **This is my site**:
1. **Site Title**: Input to change the title of the zite
2. **Site Description**: Input to change the description of the zite
3. **Save site settings**: A button, to save the last two inputs to the zites `content.json`-File
4. **Content Publishing**: A list of files you can sign (click them to insert them into the input below), an input to input the file you want to sign/publish, a button to sign the selected file, and another one, to publish it to connected peers

## Content.json File, What is It?

When a visitor visit's your zite, the first thing they download is the zite's `content.json` file. This `content.json` file holds all of the other file names which must be downloaded in order to use the zite, along with their hashes so it can be verified that they are downloading the correct files. It basically gives information on the *content* of the zite. This file also holds a cryptographic digital signature that was created by the owner to verify that the content.json file has not been tampered with by anyone other than the zite owner. 

The file does contain other information like what ZeroNet version the zite was created for, the modified number to tell what version of the zite you are downloading, the zite's title and description, the address from which you cloned the zite, and any other important information.

## Signing the Content.json File

Whenever you make any changes to your zite, including to the content.json file, you must *sign* the file. This ensures that whenever a person downloads your zite, they know these changes were made by the zite owner. Signing your content.json file will also update the hashes to all of the files stored and used on your zite.

**NOTE:** If you do not sign the `content.json` file, visitors will not be able to download this updated version of your zite for security reasons. If you have no peers, they will not be able to visit your zite at all since they can't download a *signed* `content.json` file elsewhere. So **make sure you sign this file before you publish it.**

To sign this file, you go to the sidebar and, in the `This is my site` section, click `Sign`.

## How Zites Are Kept Secure


## Publishing Your Zite

In order to publish your zite, you simply sign your `content.json` file and publish it. These buttons are located in the sidebar under the `This is my site` section. If you do not have any peers, you do not need to click publish. Publish only sends the content.json file to other peers. Without peers, there is no need because these peers will download your zite from your computer.

## Keeping Your Zite Online

In order to keep your zite online, you need peers that are reliable and always on. If your computer will not be connected to ZeroNet all the time, you will have to either have enough people to ensure your peer count won't go down to zero when you are offline, or you will have to find *at least* one peer that will always be online.

[TODO]

## Updating Your Zite

[TODO]

[^1]: There is a page on the ZeroNet Read The Docs that gives a reference to the ZeroFrame API [here](/17Kom2G5qNDc6NaQwv445h1gFzxkY3ZtZe/site_development/zeroframe_api_reference/).