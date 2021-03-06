# Zoom

|  CP Information |            |
|--------------------|------------|
| Package | Zoom 5.4.53391.1108 <br /> [Download Zoom](https://zoom.us/download?os=linux)|
| Script Name | [zoom-cp-init-script.sh](zoom-cp-init-script.sh) |
| CP Mount Path | /custom/zoom |
| CP Size | 200M |
| IGEL OS Version (min) | 11.3.110 |
| Metadata File <br /> zoom-5.4.53391.1108.inf | [INFO] <br /> [PART] <br /> file="zoom_amd64_5.4.53391.1108.tar.bz2" <br /> version="5.3.472687.1012" <br /> size="200M" <br /> minfw="11.03.110" |
| Path to Executable | /custom/zoom/usr/bin/zoom |
| Path to Icon | /custom/zoom/usr/share/pixmaps/Zoom.png |
| Missing Libraries | [libxcb-xtest0](https://packages.ubuntu.com/bionic/amd64/libxcb-xtest0) |
| Packaging Notes | Need to move the mime folder: <br /><br />mv /custom/zoom/usr/share/applications /custom/zoom/usr/share/applications.mime <br /><br />The init script needs additional files to configure AppArmor: <br /><br /> /custom/zoom/config/bin/[zoom_cp_apparmor_reload](zoom_cp_apparmor_reload) <br /> /custom/zoom/lib/systemd/system/[igel-zoom-cp-apparmor-reload.service](igel-zoom-cp-apparmor-reload.service) |

|  Customization | /wfs/user/.zoom/.zoomus.conf |
|----------------|------------------------------|
| German Language | language=de |
| French Language | language=fr |

[Supported Zoom Languages](https://support.zoom.us/hc/en-us/articles/209982306-Change-your-language-on-Zoom)

[ISO 639-1 Language Codes](https://www.loc.gov/standards/iso639-2/php/code_list.php)

Sample for setting German language (reboot required after CP deployed)
![zoomus.confg language German](zoom-zoomus.conf-lang-german.png)
