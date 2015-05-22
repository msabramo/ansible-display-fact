# ansible-display-fact
Simple shell script to display ansible facts about hosts concisely (on a single line)

# Usage

    ansible-display-fact <ansible host pattern> <ansible fact name>

# Examples

    $ ansible-display-fact analyze ansible_distribution_version
    mt2-pyweb02:                            "12.04.5 LTS, Precise Pangolin"
    mt5-ansvc01:                            "14.04.2 LTS, Trusty Tahr"
    mt1-anweb101:                           "14.04.2 LTS, Trusty Tahr"
    mt1-ansvc101:                           "14.04.2 LTS, Trusty Tahr"
    mt4-anweb101:                           "14.04.2 LTS, Trusty Tahr"
    mt3-pyweb02:                            "12.04.4 LTS, Precise Pangolin"
    mt4-ansvc01:                            "14.04.1 LTS, Trusty Tahr"
    mt5-anweb101:                           "14.04.2 LTS, Trusty Tahr"

    $ ansible-display-fact analyze ansible_system_vendor
    mt1-ansvc101:                           "OpenStack Foundation"
    mt4-ansvc01:                            "OpenStack Foundation"
    mt1-anweb101:                           "OpenStack Foundation"
    mt5-ansvc01:                            "OpenStack Foundation"
    mt4-anweb101:                           "OpenStack Foundation"
    mt3-pyweb02:                            "VMware, Inc."
    mt2-pyweb02:                            "OpenStack Foundation"
    mt5-anweb101:                           "OpenStack Foundation"

    $ ansible-display-fact analyze ansible_uptime_seconds
    mt2-pyweb02:                            10348628
    mt4-ansvc01:                            11798726
    mt1-anweb101:                           7250799
    mt5-ansvc01:                            7332084
    mt4-anweb101:                           761022
    mt3-pyweb02:                            13045033
    mt1-ansvc101:                           7250619
    mt5-anweb101:                           761020
