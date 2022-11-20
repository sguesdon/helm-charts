## Releases

{% for chartmap in site.data.index.entries %}
{%- assign sortedcharts = chartmap[1] | sort: 'created' | reverse -%}

### {{ chartmap[0] }}



| Version | Date | App. version |
{% for chart in sortedcharts %}
| [{{ chart.version }}]({{ chart.urls[0] }}) | {{ chart.created | date_to_long_string }} | {{ chart.appVersion }} |
{% endfor -%}
{% endfor %}
