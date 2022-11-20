## Releases

{% for chartmap in site.data.index.entries %}
{%- assign sortedcharts = chartmap[1] | sort: 'created' | reverse -%}

### {{ chartmap[0] }}

[Homepage](https://github.com/sguesdon/helm-charts/tree/main/charts/{{sortedcharts[0].name}})

| Version | Date | App. version |
{%- for chart in sortedcharts %}
| [{{ chart.version }}]({{ chart.urls[0] }}) | {{ chart.created | date_to_long_string }} | {{ chart.appVersion }} |
{%- endfor -%}
{% endfor %}
