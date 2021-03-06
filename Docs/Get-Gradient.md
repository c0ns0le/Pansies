---
external help file: Pansies-help.xml
Module Name: Pansies
online version: 
schema: 2.0.0
---

# Get-Gradient

## SYNOPSIS
Get a range of colors between two colors

## SYNTAX

```
Get-Gradient [-StartColor] <RgbColor> [-EndColor] <RgbColor> [[-Width] <Int32>] [[-Height] <Int32>]
 [-ColorSpace <Object>] [-Reverse] [-Flatten] [<CommonParameters>]
```

## DESCRIPTION
Get an array (or multiple arrays, one per line) of RgbColor values for a gradient from the start Color to the end Color.

## EXAMPLES

### Example 1
```
PS C:\> Get-Gradient Red Blue -Count 10 -Flatten
```

Gets a simple array of ten colors between Red and Blue.

### Example 2
```
PS C:\> Get-Gradient Red Blue
```

Gets a 2D gradient from the ConsoleColor Red to Blue, with the width x height the current size of the console.

## PARAMETERS

### -ColorSpace
A color space to render the gradient in. Defaults to HunterLab, but can be any of
CMY, CMYK, LAB, LCH, LUV, HunterLAB, HSL, HSV, HSB, RGB, XYZ, YXY

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 
Accepted values: CMY, CMYK, LAB, LCH, LUV, HunterLAB, HSL, HSV, HSB, RGB, XYZ, YXY

Required: False
Position: Named
Default value: HunterLab
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndColor
The right color to end the gradient at.

```yaml
Type: RgbColor
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Flatten
Flattens the 2D array to a single array.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Height
The number of rows to generate in the gradient. Defaults to 1

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: $Host.UI.RawUI.WindowSize.Height
Accept pipeline input: False
Accept wildcard characters: False
```

### -Reverse
For color spaces with Hue (HSL, HSV, HSB), setting this generates the gradient the long way, creating a rainbow effect.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartColor
The left color to start the gradient from.

```yaml
Type: RgbColor
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Width
The number of columns to generate in the gradient. Defaults to the width of the console.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Length, Count, Steps

Required: False
Position: 2
Default value: $Host.UI.RawUI.WindowSize.Width
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### PoshCode.Pansies.RgbColor[][]

### PoshCode.Pansies.RgbColor[]

## NOTES

## RELATED LINKS

[Get-Complement](Get-Complement.md)