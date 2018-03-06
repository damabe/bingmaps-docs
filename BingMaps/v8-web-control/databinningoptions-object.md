---
title: "DataBinningOptions Object | Microsoft Docs"
ms.custom: ""
ms.date: "02/28/2018"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4f016822-fa04-47f6-97b5-52e45cfb06ad
caps.latest.revision: 2
author: "rbrundritt"
ms.author: "richbrun"
manager: "stevelom"
---
# DataBinningOptions Object
A set options the define how a data binning layer is rendered.

| Name                | Type                                                                         | Description                                                                                                                                                                                                                                                                    |
|---------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aggregationProperty` | string                                                                       | The name of a property in the Pushpin.metadata object on which to perform calculations (average, count, sum) against the pushpins in each data bin.                                                                                                                            |
| `colorCallback`       | function (binInfo: [DataBinInfo](../v8-web-control/databininfo-object.md), min: [DataBinMetrics](../v8-web-control/databinmetrics-object.md), max: [DataBinMetrics](../v8-web-control/databinmetrics-object.md)) | A callback function which defines the color a data bin polygon should be. This callback recieves data bin information along with the min and max calculated metrics for the data set. If set, this callback function must return a color value (string color or Color object). |
| `dataBinType`         | [DataBinType](../v8-web-control/databintype-enumeration.md)                                                                  | The shape of the data bin to generate. Default: **hexagon**                                                                                                                                                                                                                    |
| `distanceUnits`       | [SpatialMath.DistanceUnits ](../v8-web-control/distanceunits-enumeration.md)                                                   | The distance units of the radius option. Default: **meters**                                                                                                                                                                                                                   |
| `polygonOptions`      | [PolygonOptions](../v8-web-control/polygonoptions-object.md)                                                               | The default options used for rendering the data bin polygons.                                                                                                                                                                                                                  |
| `radius`              | number                                                                       | A spatial distance which will be converted into a pixel distance at the equater and used to generate symetrically sized data bins that have the apprimate spatial distance radius. Default: **1000**                                                                           |
| `scaleCallback`       | function(binInfo: [DataBinMetrics](../v8-web-control/databinmetrics-object.md), min: [DataBinMetrics](../v8-web-control/databinmetrics-object.md), max: [DataBinMetrics](../v8-web-control/databinmetrics-object.md))  | A callback function which defines how much to scale a data bins size. This callback recieves data bin information along with the min and max calculated metrics for the data set. If set, this callback function must return a number between 0 and 1.                         |