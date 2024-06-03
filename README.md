# 松茸
### 目的・背景
This project aims to analyze trends and provide tools to explore relationships between various components of the livelihood framework in Shinshu, Japan. The focus is on [Matsutake Mushrooms](https://en.wikipedia.org/wiki/Matsutake) (Non-Timber Forest Products NTFPs), integrating socio-economic, socio-political, and ecological factors to support sustainable livelihoods in rural communities.


The [Sustainable Livelihood Framework](https://www.ids.ac.uk/download.php?file=files/Dp296.pdf) (SLF) provides a comprehensive model to evaluate how different factors contribute to livelihoods. This project aims to apply SLF to analyze and visualize relationships among socio-economic, socio-political, and ecological factors in Shinshu, Japan. By understanding these relationships, we can develop strategies to enhance the economic stability of rural communities and promote sustainable practices for matsutake and other NTFPs.
## Project Structure

```plaintext
matsutake/
├── main/
│   ├── data/
│   │   ├── custom_data/
│   │   │   ├── elevation_data/
│   │   │   │   └── G04-a-11_5438-jgd_GML.zip
│   │   │   ├── forest_data/
│   │   │   │   ├── 2015_agricultural_data_0.gpkg
│   │   │   │   ├── 2015_agricultural_data_1.gpkg
│   │   │   │   ├── 2018_national_forests.gpkg
│   │   │   │   └── akamatsu_filter.gpkg
│   │   │   ├── general_data/
│   │   │   │   ├── admin_boundaries_perimeter.gpkg
│   │   │   │   ├── admin_boundaries_points.gpkg
│   │   │   │   ├── shrines.gpkg
│   │   │   │   └── temples.gpkg
│   │   │   ├── pricing_data/
│   │   │   └── usage_data/
│   │   └── source_data/
│   │       ├── A12-15_2O_GML.zip
│   │       ├── A13-15_2O_GML.zip
│   │       └── A45-19_2O_GML.zip
│   │
├── projects/
│      └──  matsutake.qgz <- main QGIS entrypoint
│
├── docs/
│   └── data
│       ├── resources_mlit.md
│       └── resources_QuickOSM.md    
│
└── misc/
```

## Getting Started

### Prerequisites

- [QGIS](https://www.qgis.org/en/site/forusers/download.html)

### Recommended Plugins

To fully utilize this project, the following QGIS plugins are recommended:

- **QuickOSM**: see [resources_QuickOSM.md](docs%2Fdata%2Fresources_QuickOSM.md)
 
- **QField Sync**: this project is hosted on QFieldCloud at https://app.qfield.cloud/a/lanur622/matsutake_cloud. QFieldCoud helps with multiplatform data collection and management (https://github.com/opengisch/qfieldsync)


## Documentation
### Resource documents
- [resources_mlit.md](docs%2Fdata%2Fresources_mlit.md)
- [resources_QuickOSM.md](docs%2Fdata%2Fresources_QuickOSM.md)

### Other
- [ideas.md](docs%2Fideas.md)

- [How to add a Google Map/Terrain/Satellite Layer](https://hatarilabs.com/ih-en/how-to-add-a-google-map-in-qgis-3-tutorial)

### Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/meisei4/matsutake.git
    cd matsutake
   ```

2. Open the QGIS project:

    ```plaintext
    Open QGIS
    Go to Project > Open...
    Select `~/main/projects/matsutake.qgz`
    ```
