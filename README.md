# iOS Shared with You (SWY) Photo Library (PL) Photos.sqlite Queries
iOS Shared with You (SWY) Photo Library (PL) Photos.sqlite queries for iOS 15 and iOS 16

The [Shared with You is a new feature](https:\\www.youtube.com\watch?v=0TD96VTf0Xs) that has been discussed within Apple Worldwide Developers Conference (WWDC) videos and other developer videos. Generally, the comments made indicate that within iOS and other Apple Operating Systems this feature will allow a user to easily view and interact with links that have been shared by other users. This feature does not require users to be signed into a device with an Apple ID, nor does it require a user to have an iCloud account.

Based on what I have found, it appears to have been introduced within iOS 15, but was again discussed at [WWDC 2022](https:\\developer.apple.com\videos\play\wwdc2022\10094)

Apple discusses the Shared with You feature allows Shared assets\links to be presented to a user on a device after Apple OS has processed the shared assets\links and Apple OS determines the user might want to easily view and interact with those shared assets\links. [Currently this includes](https:\\support.apple.com\en-us\HT212721) items like:
•	Shared Music links
•	Apple TV links
•	Safari Links
•	Message media attachments
•	Podcast Links
•	News links
•	And according to documentation it appears there will be more to come…
     
My initial research, which has been published via a blog here, focuses on the Messages application and the media attachments that are presented to a user on the device as a Shared with You assets. While conducting this research, I learned Apple created a new Shared with You Syndication Photo Library. This library consists of new file system asset storage locations, a new Photos.sqlite database and much, much more! Within this write up, I will reference this photo library as the Shared with You Syndication Photo Library (SWY PL).

Even though this new Shared with You Syndication Photo Library Photos.sqlite database is very similar to the [Local Photo Library](https:\\developer.apple.com\videos\play\wwdc2021\10046) Photos.sqlite database, there are some slight differences. Based on my research, I’ve created a new set of queries to parse the data from this new Photo Library (PL) database. I have found the Shared with You Syndication Photo Library assets in devices with iOS 15.

Currently, I have only tested and researched this artifact via different iPhone models and different iOS versions. I have not completed any research about this feature within any other Apple operating systems.

This new Shared with You Syndicaion Photo Library Photos.sqlite database can be found at the following location, but only after a full file system acquisition.

\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\database\Photos.sqlite

The file system storage locations for the assets listed in the Shared with You Photos.sqlite can be found at the following locations, but again only after a full file system acquisition.

\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\scopes\syndication\originals
\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\scopes\syndication\resources\derivatives
\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\scopes\syndication\resources\derivatives\masters\

The following file system locations store only some of the assets and can be found in an iTunes back-up acquisition(s):

\private\var\mobile\Media\PhotoData\UBF\scopes\syndication\originals
\private\var\mobile\Media\PhotoData\UBF\scopes\syndication\resources\derivatives
\private\var\mobile\Media\PhotoData\UBF\scopes\syndication\resources\derivatives\masters\

