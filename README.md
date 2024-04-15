[![arXiv](https://img.shields.io/badge/arXiv-1234.56789-b31b1b.svg)](https://arxiv.org/abs/2402.14958)
# EE3P: Event-based Estimation of Periodic Phenomena Properties
Kolář, J., Špetlík, R., Matas, J. (2024) Measuring Speed of Periodical Movements with Event Camera. In Proceedings of the 27th Computer Vision Winter Workshop, 2024

Paper Link: [arXiv](https://arxiv.org/abs/2402.14958), [CVWW proceedings](https://cvww2024.sdrv.si/wp-content/uploads/sites/5/2024/02/CVWW2024_Proceedings.pdf)

Data Capture Demonstration: [Video](https://youtu.be/QlfQtvbaYy8)

![Method's diagram](https://github.com/JackPieCZ/EE3P/assets/72486584/6a8b1c87-4ad4-4923-9bd3-48d17101067c)

1. Data captured from an event camera is aggregated into non-overlapping arrays along the time axis,    
2. A region of Interest and a template are selected, 
3. 2D correlation of the template with arrays is computed,
4. The frequency is calculated from the average of time deltas measured between correlation peaks.


## Data Structure: 🗃

The data is organized into folders, each representing a specific experiment from the paper. Each folder contains the following files:

- `.raw`: Raw event camera data in the [EVT  3.0](https://docs.prophesee.ai/stable/data/encoding_formats/evt3.html#chapter-data-encoding-formats-evt3) format.
- `_slowdownfactor_fps.avi`: Slowed down video of the event stream.
- `_tachometer_data.xml`: Ground truth data from the laser tachometer (if applicable).

The files were compressed and split into multiple `.rar` files to meet GitHub file size guidelines.

### Folder Descriptions: 📁

- `01_line`: Experiment measuring the rotational speed of a disc with a high-contrast mark.
- `02_velcro`: Experiment measuring the rotational speed of a disc with a uniform velcro surface.
- `03_velcroside`: Experiment measuring the rotational speed of a disc with velcro, viewed from the side.
- `04_speaker`: Experiment measuring the vibration frequency of a speaker diaphragm.
- `05_led`: Experiment measuring the flashing frequency of an LED.

**Note:** 
Not all experiments use the laser tachometer, hence the absence of the corresponding data file in some folders.

## Usage: 🚀

The data can be used for various purposes, including:
- Reproducing the experiments in the paper.
- Developing and testing new methods for frequency and rotational speed estimation using event cameras.
- Comparing the performance of different event camera-based methods.

## License: 📄

The data is provided under the GPL-3.0 license. Please refer to the LICENSE file for details.

We encourage you to use this data responsibly and cite the paper if you use it in your work:
```
@misc{kolář2024ee3p,
      title={EE3P: Event-based Estimation of Periodic Phenomena Properties}, 
      author={Jakub Kolář and Radim Špetlík and Jiří Matas},
      year={2024},
      eprint={2402.14958},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```

