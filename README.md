# php-cpsk-api
Api to fetch 3 nearest departures from cp.sk

Inspired by official [python version](https://github.com/Adman/python-cpsk-api).

# Usage

```
use JozefCipa\CP\CpSK;
use JozefCipa\CP\CpException;

$cpsk = new CpSK;

$departures = $cpsk->from('Pod Táborom')
	    		->to('Čierny most')
	    		->useVehicles(CpSK::MHD)
	    		->inCity('Prešov')
	    		->at('12:00 13.03.2017')
	    		->find();
```

**Note:** Stops names must match exact name available on cp.sk

Credits: [Official creator](https://github.com/Adman/)

Beware that by using this you might be violating cp.sk ToS
