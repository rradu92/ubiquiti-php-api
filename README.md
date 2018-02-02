# ubiquiti-php-api

Usage example:

$ubiquiti = new Ubiquiti('192.168.1.2', 'ubnt', 'ubnt', true, '443', 3);

print_r($ubiquiti->stations($array)); 
Get the list of all stations connected to the AP

print_r($ubiquiti->status($array));
Get the AP dashboard status

print_r($ubiquiti->status_new($array)); 
Get the interface status

print_r($ubiquiti->ifstats($array));
Get interfaces rx/tx bytes and uptime of host

print_r($ubiquiti->iflist($array));
Practically same as status_new

print_r($ubiquiti->brmacs($array));
Get bridge table

print_r($ubiquiti->spectrum(10, $array));
Do a spectrum first value is timeout in seconds, usually more that the 3secs limit to query anything
Be careful if you have connected stations, will temporally desregister

print_r($ubiquiti->signal(true));
Get signal status

print_r($ubiquiti->air_view(true));
Get the airview status

print_r($ubiquiti->station_kick('AA:BB:CC:DD:EE:FF', 'ath0', $array));
Kick out a station connected to the AP, have to specify the MAC address and the interface, usually ath0

Set variable $array to true if want to return array, or leave empty/set false to get json
