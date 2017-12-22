# SinusBot API PHP-Class

> PHP-Class for the SinusBot (http://sinusbot.com)

You can retrieve information with the PHP-Class. It is now possible to view the current status and the current title of the track or stream on your own homepage via PHP.

The PHP-Class is compatible with the hosting version, you can use e.g. [TS3index.com](https://ts3index.com/hosting/product/teamspeak-3-musicbot.html) musicbots

#### Example: Connect

```php
include("sinusbot.class.php");
$sinusbot = new SinusBot("http://127.0.0.1:8087");
$sinusbot->login("admin", "foobar");
```

#### Functions:

The parameter $instanceUUID is optional for every function having this parameter. However, if omitting it, you must have selected the instance via `$sinusbot->selectInstance("INSTANCEUUID")` beforehand.

```php
$sinusbot = new SinusBot("http://127.0.0.1:8087");
$sinusbot->login($username, $password)
$sinusbot->getFiles()
$sinusbot->getRadioStations($search)
$sinusbot->getStatus($instanceUUID)
$sinusbot->getInfos()
$sinusbot->getInstanceLog($instanceUUID)
$sinusbot->getPlaylists()
$sinusbot->createPlaylist($playlistName)
$sinusbot->renamePlaylist($playlistName, $playlistUUID)
$sinusbot->deletePlaylist($playlistUUID)
$sinusbot->getPlaylistTracks($playlistUUID)
$sinusbot->addPlaylistTrack($trackUUID, $playlistUUID)
$sinusbot->deletePlaylistTrack($trackPosition, $playlistUUID)
$sinusbot->deletePlaylistTracks($playlistUUID)
$sinusbot->getQueueTracks($instanceUUID)
$sinusbot->appendQueueTrack($trackUUID, $instanceUUID)
$sinusbot->prependQueueTrack($trackUUID, $instanceUUID)
$sinusbot->deleteQueueTrack($trackUUID, $instanceUUID)
$sinusbot->deleteQueueTracks($instanceUUID)
$sinusbot->say($text, $locale, $instanceUUID)
$sinusbot->playTrack($trackUUID, $instanceUUID)
$sinusbot->playURL($url, $instanceUUID)
$sinusbot->playPlaylist($playlistUUID, $playlistIndex, $instanceUUID)
$sinusbot->playPrevious($instanceUUID)
$sinusbot->playNext($instanceUUID)
$sinusbot->playRepeat($repeatState, $instanceUUID)
$sinusbot->playShuffle($shuffleState, $instanceUUID)
$sinusbot->stop($instanceUUID) 
$sinusbot->seekPlayback($position, $instanceUUID)
$sinusbot->getPlayedTracks($instanceUUID)
$sinusbot->moveTrack($trackUUID, $parent)
$sinusbot->editTrack($trackUUID, $title, $artist, $album)
$sinusbot->deleteTrack($trackUUID)
$sinusbot->getVolume($instanceUUID) 
$sinusbot->setVolume($volume, $instanceUUID)
$sinusbot->setVolumeUp($instanceUUID)
$sinusbot->setVolumeDown($instanceUUID)
$sinusbot->addURL($url, $title, $parent)
$sinusbot->addFolder($folderName, $parent)
$sinusbot->moveFolder($folderUUID, $parent)
$sinusbot->renameFolder($folderName, $folderUUID)
$sinusbot->deleteFolder($folderUUID)
$sinusbot->getJobs()
$sinusbot->addJob($URL)
$sinusbot->deleteJob($jobUUID)
$sinusbot->deleteFinishedJobs()
$sinusbot->uploadTrack($path)
$sinusbot->uploadAvatar($path, $instanceUUID)
$sinusbot->deleteAvatar($instanceUUID)
$sinusbot->getUsers()
$sinusbot->addUser($username, $password, $privileges)
$sinusbot->setUserPassword($password, $userUUID)
$sinusbot->setUserPrivileges($privileges, $userUUID)
$sinusbot->setUserIdentity($identity, $userUUID)
$sinusbot->setUserServergroup($groupID, $userUUID)
$sinusbot->deleteUser($userUUID)
$sinusbot->getSettings($instanceUUID)
$sinusbot->editSettings($data, $instanceUUID)
$sinusbot->getChannels($instanceUUID)
$sinusbot->getInstances()
$sinusbot->selectInstance($instanceUUID)
$sinusbot->createInstance($nickname)
$sinusbot->deleteInstance($instanceUUID)
$sinusbot->spawnInstance($instanceUUID)
$sinusbot->respawnInstance($instanceUUID)
$sinusbot->killInstance($instanceUUID)
$sinusbot->getWebStream($instanceUUID)
$sinusbot->getWebStreamToken($instanceUUID)
$sinusbot->getDefaultBot()
$sinusbot->getBotLog()
$sinusbot->getThumbnail($thumbnail)
$sinusbot->isPlaying($instanceUUID)
$sinusbot->isRunning($instanceUUID)
```
