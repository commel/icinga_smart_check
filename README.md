# Icinga Check for smartctl

## Requirements
This check only requires Python 3.6 (openSUSE Leap 15.4 based) and smartctl. Place it somewhere accessible for Icinga.

## Arguments

	./check_smart2 -device /dev/sda -read_error_warn=1000 -read_error_crit=10000

* -read_error_warn triggers warning if errors exceed value
* -read_error_crit triggers critical if errors exceed value
* -temperature_warn warning if temperature exceeds value
* -temperature_crit critical if temperature exceeds value
* -value-fmt formatting raw-values from vendor specific values
  (e.g. ```1,raw48:54``` formats field 1)
* -debug True activates debugging mode

## Installation
Place the check_smart2 somewhere where Icinga can access it (e.g. /usr/local/bin). Then append the
content of ```services.conf``` and ```commands.conf``` to your Icinga files.
