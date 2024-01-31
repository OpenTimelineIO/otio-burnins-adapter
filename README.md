# OpenTimelineIO Burnins Adapter
[![Build Status](https://github.com/OpenTimelineIO/otio-burnins-adapter/actions/workflows/ci.yaml/badge.svg)](https://github.com/OpenTimelineIO/otio-burnins-adapter/actions/workflows/ci.yaml)
![Dynamic YAML Badge](https://img.shields.io/badge/dynamic/yaml?url=https%3A%2F%2Fraw.githubusercontent.com%2FOpenTimelineIO%2Fotio-burnins-adapter%2Fmain%2F.github%2Fworkflows%2Fci.yaml&query=%24.jobs%5B%22test-plugin%22%5D.strategy.matrix%5B%22otio-version%22%5D&label=OpenTimelineIO)
![Dynamic YAML Badge](https://img.shields.io/badge/dynamic/yaml?url=https%3A%2F%2Fraw.githubusercontent.com%2FOpenTimelineIO%2Fotio-burnins-adapter%2Fmain%2F.github%2Fworkflows%2Fci.yaml&query=%24.jobs%5B%22test-plugin%22%5D.strategy.matrix%5B%22python-version%22%5D&label=Python)

The `burnins` adapter is part of OpenTimelineIO's adapter plugins.
Uses FFmpeg to burn text overlays into video media.

# Usage
Add your own variation of the following setup to the Timeline's metadata

``` json 
"metadata": {
    "burnins": {
        "overwrite": true,
        "burnins": [
            {
                "text": "Top Center",
                "align": "top_centered",
                "font": "/System/Library/Fonts/Menlo.ttc",
                "font_size": 48,
                "function": "text"
            },
            {
                "align": "top_left",
                "x_offset": 75,
                "font": "/System/Library/Fonts/Menlo.ttc",
                "frame_offset": 101,
                "font_size": 48,
                "function": "frame_number"
            }
        ],
        "streams": [
            {
                "codec_type": "video",
                "codec_name": "h264",
                "width": 1920,
                "height": 1080,
                "r_frame_rate": "30/1",
                "start_time": "0.000000",
                "duration": "20.000000"
            }
        ]
    }
```
# License

OpenTimelineIO and the "burnins" adapter are open source software.
Please see the [LICENSE](LICENSE) for details.

Nothing in the license file or this project grants any right to use Pixar or
any other contributor’s trade names, trademarks, service marks, or product names.

# Contributions

If you want to contribute to the project,
please see: https://opentimelineio.readthedocs.io/en/latest/tutorials/contributing.html  
Please also read up on [testing your code](https://github.com/OpenTimelineIO/otio-plugin-template#testing-your-plugin-during-development) 
in the "getting started" section of the OpenTimelineIO plugin template repository.

# Contact

For more information, please visit http://opentimeline.io/
or https://github.com/AcademySoftwareFoundation/OpenTimelineIO
or join our discussion forum: https://lists.aswf.io/g/otio-discussion
