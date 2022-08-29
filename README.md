# iOS Shared with You (SWY) Photo Library (PL) Photos.sqlite Queries
iOS Shared with You (SWY) Photo Library (PL) Photos.sqlite queries for iOS 15 and iOS 16

[Shared with You is a new feature] (https://developer.apple.com/videos/play/wwdc2022/10094/) within iOS and other Apple Operating Systems that allows a user to easily view and interact with links that have been shared by other users. This feature does not require users to be signed into a device with an Apple ID, nor does it require a user to have an iCloud account.

Shared assets/links are presented to the user on a device after Apple OS has processed the shared assets/links and Apple OS determines the user might want to easily view those shared assets/links. [Currently this includes] (https://support.apple.com/en-us/HT212721) items like:
•	Shared Music links
•	Apple TV links
•	Safari Links
•	Message media attachments
•	Podcast Links
•	News links
•	And according to documentation it appears there will be more to come…
     
My initial research, which will be published via a blog can be found here and focuses on the Messages application and the media attachments that are presented to a user on the device as a Shared with You asset. While conducting this research, I learned within this feature, Apple created a new Shared with You Photo Library that consists of new file system asset storage locations, a new Photos.sqlite database and much, much more! 

Even though this new Photos.sqlite database is very similar to the [Local Photo Library] (https://developer.apple.com/videos/play/wwdc2021/10046/) Photos.sqlite database, there are slight differences. Based on my research, I have created a new set of queries to parse the data from the databases. Based on what I’ve observed during research, testing, and Apple Development documentation Shared with You feature can be found starting with iOS 15.0.

Currently, I have only tested and researched this artifact via different iPhone models and different versions of the iOS operating system. I have not researched this feature, file system storage or database activity on MacBook’s, Mac OS, or any other Apple operating systems.

This new Shared with You Photo Library Photos.sqlite database can be found at the following location, but only after a full file system acquisition.

•	\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\database\Photos.sqlite

The file system storage locations for the assets listed in the Shared with You Photos.sqlite can be found at the following locations, but again only after a full file system acquisition.

•	\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\scopes\syndication\originals\
•	\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\scopes\syndication\resources\derivatives\
•	\private\var\mobile\Library\Photos\Libraries\Syndication.photoslibrary\scopes\syndication\resources\derivatives\masters\

The following file system locations store only some of the assets and can be found in a Logical/iTunes backup acquisition(s):

•	\private\var\mobile\Media\PhotoData\UBF\scopes\syndication\originals\
•	\private\var\mobile\Media\PhotoData\UBF\scopes\syndication\resources\derivatives\
•	\\private\var\mobile\Media\PhotoData\UBF\scopes\syndication\resources\derivatives\masters\
