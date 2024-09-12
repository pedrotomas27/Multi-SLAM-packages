# SLAM Methods with LiDAR Support

This repository includes implementations of eight different SLAM methods tested with two datasets, one using Velarray M1600, the other using Bpearl. Due to compatibility issues with the LiDAR technologies used, most methods required modifications to handle both datasets. Unfortunately, not all methods were successfully adapted.

## LiDAR Compatibility

The following table summarizes the success of package adaptation and data transformation for each SLAM method. For methods that could not be effectively modified, two Python nodes have been created to transform each LiDAR dataset into a more commonly used technology, VLP-16. Depending on your machine’s capability, real-time transformations may be possible.

### Compatibility Table

| **SLAM Method**  | **Package Adaptation** | **Data Transformation** |
|------------------|------------------------|--------------------------|
| FAST-LIO2        | ✔️*                    | ✔️                       |
| Light-LOAM       | ✔️                     | ✔️                       |
| iG-LIO           | ✔️                     | ✔️                       |
| Point-LIO        | ✔️*                    | ✔️                       |
| Faster-LIO       | ✔️                     | ✔️                       |
| A-LOAM           | ✔️                     | ✔️                       |
| DLIO             | ✔️                     | ✔️                       |
| DLO              | ✔️                     | ✔️                       |

Note: ✔️*  - Success was achieved only with Velarray M1600. Methods do not support Bpearl technology.
*DLO and DLIO already supported the tested LiDAR technology.
### Usage Instructions

1. **Transform Data**: For SLAM methods that do not directly support Velarray M1600 or Bpearl LiDAR technology, use the provided Python nodes to convert your data into the VLP-16 format.
2. **Run SLAM Methods**: Execute the SLAM methods according to their respective instructions. Ensure to run any necessary transformation nodes concurrently if required.

## Docker

The methods are available as Docker images. You can find them at [Docker Hub](https://hub.docker.com/repository/docker/pedrotomas2700/rustle/general).

## Dependencies

The tested environment was ROS Noetic with Ubuntu 20.04. For specific package dependencies, please refer to the GitHub repository of each SLAM method.
