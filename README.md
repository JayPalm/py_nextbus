A minimalistic Python 3 client to simplify making requests to the NextBus API. Response content can be returned as either JSON or XML, using the respective NextBus public feed.

All commands in the NextBus API as of revision 1.23 are supported.

See the NextBus XML feed documentation for more information: https://www.nextbus.com/xmlFeedDocs/NextBusXMLFeed.pdf

Note: Other than the output format, the NextBus XML feed and JSON feeds are the same. The XML feed documentation also applies to the JSON feed.

Installation
---

Install with Pip:

`pip install py-nextbus`

Usage
---

```python
import py_nextbus
client = py_nextbus.NextBusClient(output_format='json')
agencies = client.get_agency_list()

client = py_nextbus.NextBusClient(output_format='json', agency='ucb')
client.get_route_list()

client.get_route_config('peri')
client.get_predictions(stop_tag='tolmhall', route_tag='peri',)
```
