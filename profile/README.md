Glottography is a collection of datasets providing information about the spatial extent of *speaker areas*, i.e., the areas where particular languages are spoken.

Each dataset is derived from geographic maps published in a *source publication* as follows:
1. The shapes depicted in the source maps are turned into [GIS vector objects](https://en.wikipedia.org/wiki/Data_model_(GIS)#Vector_data_model).
2. The metadata provided in the source publication is used to match the shape to a [languoid](https://glottolog.org/glottolog/glottologinformation)
   in the [Glottolog](https://glottolog.org) catalog.

> [!NOTE]
> Multiple features in the source may be mapped to the same Glottolog languoid.

This information is packaged into a [CLDF](https://cldf.clld.org) dataset (in the `cldf` subdirectory of each dataset) in order to provide interoperable data for cross-linguistic analyses as follows:
- The metadata of the shapes (aka [features](https://datatracker.ietf.org/doc/html/rfc7946#section-3.2) in GeoJSON terminology) are listed in a
  [ContributionTable](https://github.com/cldf/cldf/tree/master/components/contributions) with a link to the GeoJSON file containing the shape.
- A [LanguageTable](https://github.com/cldf/cldf/tree/master/components/languages) lists the language- and family-level languoids for which the dataset
  provides information (via features either directly mapped to the languoid or mapped to "parts" of the languoid, i.e., dialects or sub-groups) with
  links to the features in the source that were aggregated.
- Three sets of geo-data:
  - The features as depicted in the source publication.
  - Aggregated language-level speaker areas.
  - Aggregated family-level speaker areas.
 
Reviewed and released datasets are published in the [Glottography community on Zenodo](https://zenodo.org/communities/glottography).
