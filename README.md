# VIDEO CONVERTER

install this first, this is installed in windows
https://github.com/BtbN/FFmpeg-Builds/releases

```
$dirPath = "C:\DELETEABLE\video-converter\to-covert" # replace with your directory path
$outputDir = "C:\DELETEABLE\video-converter\converted" # replace with your output directory path
Get-ChildItem -Path $dirPath -Filter *.mov | ForEach-Object {
    $baseName = ($_ | Get-Item).BaseName
    & ffmpeg -i "$dirPath\\$($_.Name)" -vcodec h264 -acodec aac "$outputDir\\$baseName.mp4"
}
```
