# C# Parser add-ons

C# Parser add-ons are used to import C# script to uNode.

Before using C# Parser you need to import this add-ons, navigate to `Tools > uNode > Welcome > Add-ons` and click on the `C# Parser` to import the add-ons.

To open C# Parser, navigate to `Tools > uNode > C# Parser`

## Parsing C# Scripts from the project

1. Open C# Parser window
2. Select `From MonoScript` category
3. Assign the `Scripts` field with the c# script you want to parse
4. (Optionally) you can batch add c# script from a folder by selecting `Batch Add Scripts From Folder`
5. Click `Parse` to begin parsing the scripts.

> [!NOTE]
> This is the most stable for parsing a c# scripts

## Parsing C# Script from texts

1. Open C# Parser window
2. Select `From Source` category
3. Paste the c# source code to the `Script` field.
5. Click `Parse` to begin parsing the scripts.

> [!CAUTION]
> The c# source code must not give an error when the script is placed on the project, otherwise the parse will not work.

## Parsing C# Script from File

1. Open C# Parser window
2. Select `From File` category
3. Click `Load File` and select the c# script file in your disk.
5. Click `Parse` to begin parsing the scripts.

> [!CAUTION]
> The c# file must not give an error when the script is placed on the project, otherwise the parse will not work.