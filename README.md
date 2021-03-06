# Umbraco Image Crop Picker #

[![Build status](https://ci.appveyor.com/api/projects/status/ladurl50o0c40r7c/branch/master?svg=true)](https://ci.appveyor.com/project/mzajkowski/umbraco-image-crop-picker/branch/master) [![NuGet Version](https://img.shields.io/nuget/v/Our.Umbraco.ImageCropPicker)](https://www.nuget.org/packages/Our.Umbraco.ImageCropPicker/)


**Custom proprty editor for selecting single (currently) image crop data record from customizable Image Cropper DataType.**

## Example usage ##

You need to have data type in your solution which is using Image Cropper property editor built in Umbraco. It may be default Image Cropper DataType, but also your custom one.

![](docs/img/example-0.png?raw=true)

After installation of _Our.Umbraco.ImageCropPicker_ you'll be able to create new DataType using Image Crop Picker property editor. You need to specify which DataType with Image Cropper you want to use in this one and from which we'll be retrieving image crops data.

![](docs/img/example-1.png?raw=true)

Brand new DataType is ready to be used on any DocumentType created inside Umbraco solution.

![](docs/img/example-2.png?raw=true)

![](docs/img/example-3.png?raw=true)

Using included property value converter it's possible to retrieve property value as a strongly typed ImageCropData model delivered by default with Umbraco.

	var cropPickerData = Model.Content.GetPropertyValue<ImageCropData>("cropPicker");

	var alias = cropPickerData.Alias;
	var width = cropPickerData.Width;
	var height = cropPickerData.Height;
	var coordinates = cropPickerData.Coordinates;

## Installation ##

### NuGet package repository

To [install from NuGet](https://www.nuget.org/packages/Our.Umbraco.ImageCropPicker), you can run the following command from within Visual Studio:

```
PM> Install-Package Our.Umbraco.ImageCropPicker
```