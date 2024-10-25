# How-to-Turn-Off-Lenovo-Conservative-mode-using--linux
Find the path for the conservation mode setting in /sys/bus/platform/drivers/ideapad_acpi using ls /sys/bus/platform/drivers/ideapad_acpi.

In my case, the path is
/sys/bus/platform/drivers/ideapad_acpi/VPC2004:00/conservation_mode

You can then run (adjusting the path as needed)

echo 0 | sudo tee /sys/bus/platform/drivers/ideapad_acpi/VPC2004:00/conservation_mode

1 means conservation mode is active. Change it to 0 to disable it.
