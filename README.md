# iOS_Shared_with_You_Photo_Library_Photos.sqlite_Queries
iOS Shared with You Photo Library Photos.sqlite queries

[Shared with You is a new feature] (https://developer.apple.com/videos/play/wwdc2022/10094/) within iOS and other Apple Operation Systems that allows a user to easily view and interact with items that have been shared by other users. This feature does not require users to be signed into a device with an Apple ID, nor does it require an iCloud account. 

Shared assets are presented to the user on a device based on Apple data processing of those shared assets. [Currently this includes] (https://support.apple.com/en-us/HT212721) items like:
•	Shared Music links
•	Apple TV links
•	Safari Links
•	Message media attachments
•	Podcast Links
•	News links
•	And according to documentation it appears there will be more to come…
     
My initial research, which has been published via a blog can be found here and focuses on the Shared with You messages media attachments. While conducting this research, I learned within the creation of this new Shared with You feature, Apple created a new Shared with You Photo Library that consists of new file system asset storage location, a new Photos.sqlite database and much, much more! 

Even though this database is very similar to the [Local Photo Library] (https://developer.apple.com/videos/play/wwdc2021/10046/) Photos.sqlite database, there are slight differences and I have created a new set of queries to parse the data from the database. Based on what I’ve observed during research, testing, and Apple Development documentation this Shared with You feature can be found starting in iOS 15.0.

Currently, I have only tested and researched this artifact via several different iPhones and the iOS operating system.

This new Shared with You Photo Library Photos.sqlite database can be found at the following location only after a full file system acquisition.

•	\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\database\Photos.sqlite

The file system storage locations for the assets listed in the Shared with You Photos.sqlite can be found at the following locations only after a full file system acquisition.

•	\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\scopes\syndication\originals\
•	\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\scopes\syndication\resources\derivatives\
•	\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\scopes\syndication\resources\derivatives\masters\

The following file system locations store only some of the assets and can be found in a Logical / iTunes backup acquisition:

•	\private\var\mobile\Media\PhotoData\UBF\scopes\syndication\originals\
•	\private\var\mobile\Media\PhotoData\UBF\scopes\syndication\resources\derivatives\
•	\\private\var\mobile\Media\PhotoData\UBF\scopes\syndication\resources\derivatives\masters\
