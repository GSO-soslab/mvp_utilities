# A suite of localization nodes

### Dependency
- GeographicLib
```
sudo apt install geographiclib-tools
sudo apt install libgeographic-dev
```

- for magnetic model installation please check this link
```
https://geographiclib.sourceforge.io/C++/doc/magnetic.html
```
- download the `WMM2020` model then do the following
```
sudo mkdir -p /usr/local/share/GeographicLib
sudo tar xofjC wmm2020.tar.bz2 /usr/local/share/GeographicLib
```

- For PI you need to copy the file to a different directory
```
sudo tar xofjC wmm2020.tar.bz2 /usr/local/share/GeographicLib
```

## Note:
We have implemented the rosparam for the magnetic model pat.
you can do something below in your launch file now.

```
<param name = "mag_model_path" value = "$(find mvp_localization_utilities)/config/magnetic"/>
```