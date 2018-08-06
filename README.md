# ACThumbnailGenerator            
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Platform](https://img.shields.io/badge/platform-iOS--tvOS-br.svg)
![Language](https://img.shields.io/badge/language-Objective--C-brightgreen.svg )

ACThumbnailGenerator is a simple and easy-to-use utility for extracting still images from remote video streams (specially for HLS / m3u8 streams).

## Installation and Setup

#### Manual
Just drag the ACThumbnailGenerator folder to your project.

## Usage
```objective-c

double bitRate = 1000000; // force video bit rate (can be use to cap video quality and improve performance). Pass 0 to use default bit rate.
self.thumbnailGenerator = [[ACThumbnailGenerator alloc] initWithPreferredBitRate:bitRate];

NSURL *videoURL = [NSURL URLWithString:@"http://qthttp.apple.com.edgesuite.net/1010qwoeiuryfg/sl.m3u8"];
int position = 10; // video position (in seconds) from where thumbnail should be extracted. Always pass 0 for live streams.

[self.thumbnailGenerator loadImageFrom:videoURL position:position withCompletionBlock:^(UIImage *image) {

    // use `image`            

}];

```

### Licensing
This project is licensed under the terms of the MIT license.
