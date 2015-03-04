# Subprefectures of  São Paulo

In Brazil, *[prefectures]* are the executive branch of the government of each Brazilian municipality. Some big cities, like [São Paulo], have administrative divisions called ***[subprefectures]***.

This repository holds basic data about [São Paulo's subprefectures]. The [city prefecture] published georeferenced administrative limits at [Mapa Digital do Cidade web page], and this data is available here in the following formats:

* [GeoJSON](../../raw/master/data/subprefeituras-sp.geojson) [(?)](https://en.wikipedia.org/wiki/GeoJSON)
* [TopoJSON][TopoJSON file] [(?)][TopoJSON]
* [KML][KML file] [(?)][KML]

Visit this [map preview] to see the data .

If you find errors, please [open an issue].

## The data

Each item has a polygon representing subprefecture's limits and the following properties:

* ***id***: an identifier code used by the prefecture, accordingly to [MDC][Mapa Digital do Cidade web page];
* ***name***: the subprefecture name, as spelled at [this page][São Paulo's subprefectures];
* ***area***: total area, in *km2* (source: [IBGE][demography data]);
* ***pop_2010***: population in 2010 (source: [IBGE][demography data]);
* ***pop_density_2010***: pop_2010 divided by area (hab/km2);
* ***budget_2015***: total budget for 2015 (source: [2015 Budget Law]);
* ***DATA_CRIAC***: there is no documentation about this property, it is probably when the [MDC files][Mapa Digital do Cidade web page] were generated;
* ***DATA_ULT_A***: there is no documentation about this property, it is probably the last time the administrative limits changed;


This data was edited using [QGIS] and the following command was used to generate the [TopoJSON] file:

```
topojson -p -o subprefeituras-sp.topojson subprefeituras-sp.geojson
```


[subprefectures]: https://en.wikipedia.org/wiki/Subprefecture#Brazil
[prefectures]: http://en.wikipedia.org/wiki/Prefecture#Brazilian_equivalent_of_prefecture
[city prefecture]: http://www.prefeitura.sp.gov.br/
[São Paulo's subprefectures]: http://www.prefeitura.sp.gov.br/cidade/secretarias/subprefeituras/subprefeituras/index.php?p=8978
[map preview]: https://github.com/codigo-urbano/subprefeituras-sp/blob/master/data/subprefeituras-sp.topojson
[open an issue]: https://github.com/codigourbano/subprefeituras-sp/issues
[São Paulo]: https://en.wikipedia.org/wiki/S%C3%A3o_Paulo
[Mapa Digital do Cidade web page]: http://www.prefeitura.sp.gov.br/cidade/secretarias/desenvolvimento_urbano/dados_estatisticos/index.php?p=160798
[QGIS]: http://www.qgis.org
[TopoJSON]: https://github.com/mbostock/topojson/wiki
[TopoJSON file]: ../../raw/master/data/subprefeituras-sp.topojson
[KML]: http://en.wikipedia.org/wiki/Keyhole_Markup_Language
[KML file]: ../../raw/master/data/subprefeituras-sp.kml
[2015 budget law]: http://sempla.prefeitura.sp.gov.br/orcamento/loa.html
[demography data]: http://www.prefeitura.sp.gov.br/cidade/secretarias/subprefeituras/subprefeituras/dados_demograficos/
