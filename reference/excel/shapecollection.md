# ShapeCollection Object (JavaScript API for Excel)

Represents all the shapes in the worksheet.

## Properties

| Property	   | Type	|Description| Req. Set|
|:---------------|:--------|:----------|:----|
|items|[Shape[]](shape.md)|A collection of shape objects. Read-only.|[beta](../requirement-sets/excel-api-requirement-sets.md)|

_See property access [examples.](#property-access-examples)_

## Relationships
None


## Methods

| Method		   | Return Type	|Description| Req. Set|
|:---------------|:--------|:----------|:----|
|[addGeometricShape(geometricShapeType: string, left: double, top: double, width: double, height: double)](#addgeometricshapegeometricshapetype-string-left-double-top-double-width-double-height-double)|[Shape](shape.md)|Adds a geometric shape to worksheet. Returns a Shape object that represents the new shape.|[beta](../requirement-sets/excel-api-requirement-sets.md)|
|[addImage(base64ImageString: string)](#addimagebase64imagestring-string)|[Image](image.md)|Creates an image from a base64 string and adds it to worksheet. Returns the image object that represents the new Image.|[beta](../requirement-sets/excel-api-requirement-sets.md)|
|[addTextBox(text: string)](#addtextboxtext-string)|[Shape](shape.md)|Adds a textbox to worksheet by telling it's text content. Returns a Shape object that represents the new text box.|[beta](../requirement-sets/excel-api-requirement-sets.md)|
|[getCount()](#getcount)|int|Returns the number of shapes in the worksheet. Read-only.|[beta](../requirement-sets/excel-api-requirement-sets.md)|
|[getItem(shapeId: string)](#getitemshapeid-string)|[Shape](shape.md)|Returns a shape identified by the shape id. Read-only.|[beta](../requirement-sets/excel-api-requirement-sets.md)|

## Method Details


### addGeometricShape(geometricShapeType: string, left: double, top: double, width: double, height: double)
Adds a geometric shape to worksheet. Returns a Shape object that represents the new shape.

#### Syntax
```js
shapeCollectionObject.addGeometricShape(geometricShapeType, left, top, width, height);
```

#### Parameters
| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|geometricShapeType|string|Represents the geometric type of the shape.|
|left|double|The distance, in points, from the left side of the shape to the left side of the worksheet.|
|top|double| The distance, in points, from the top edge of the shape to the top of the worksheet.|
|width|double|The width, in points, of the shape.|
|height|double|The height, in points, of the shape.|

#### Returns
[Shape](shape.md)

### addImage(base64ImageString: string)
Creates an image from a base64 string and adds it to worksheet. Returns the image object that represents the new Image.

#### Syntax
```js
shapeCollectionObject.addImage(base64ImageString);
```

#### Parameters
| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|base64ImageString|string|A base64 encoded image in JPEG or PNG formats.|

#### Returns
[Image](image.md)

### addTextBox(text: string)
Adds a textbox to worksheet by telling it's text content. Returns a Shape object that represents the new text box.

#### Syntax
```js
shapeCollectionObject.addTextBox(text);
```

#### Parameters
| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|text|string|Optional. Represents the text that will be shown in the created text box.|

#### Returns
[Shape](shape.md)

### getCount()
Returns the number of shapes in the worksheet. Read-only.

#### Syntax
```js
shapeCollectionObject.getCount();
```

#### Parameters
None

#### Returns
int

### getItem(shapeId: string)
Returns a shape identified by the shape id. Read-only.

#### Syntax
```js
shapeCollectionObject.getItem(shapeId);
```

#### Parameters
| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|shapeId|string|The identifier for the shape.|

#### Returns
[Shape](shape.md)
