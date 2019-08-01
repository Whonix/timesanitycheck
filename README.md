# Checks if the system clock is sane between build timestamp and expiration date #

Reports, if clock is sane and not slower than build timestamp or faster than
expiration date (configurable, default currently set to 17 MAY 2033 10:00:00).

This should catch situations, where the host's clock is too much off (CMOS
battery defect, user mistakenly set a very wrong date, etc.), resulting in
network time synchronization tools (such as sdwdate) no longer being able to
correct the clock; catch eventual bigger bugs in network time synchronization
tools; and some types of attacks on network time synchronization.
## How to install `timesanitycheck` using apt-get ##

1\. Download [Whonix's Signing Key]().

```
wget https://www.whonix.org/patrick.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add Whonix's signing key.

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg add ~/patrick.asc
```

3\. Add Whonix's APT repository.

```
echo "deb https://deb.whonix.org buster main contrib non-free" | sudo tee /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `timesanitycheck`.

```
sudo apt-get install timesanitycheck
```

## How to Build deb Package ##

Replace `apparmor-profile-torbrowser` with the actual name of this package with `timesanitycheck` and see [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/apparmor-profile-torbrowser).

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`timesanitycheck` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
