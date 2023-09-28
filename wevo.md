# Wevo

## Search Dynamic Storage by regex
```
await _wevo.dynamicStorage.listAsync("bawLinxSubgroupToVtexCategory", 1, 100, { regex: [{ "linxSubgroup": `/^${productLinxSubgroup}\$/i` }] });
```

## Required dynamic storage key
```
let linxColorToVtexColor = await _wevo.dynamicStorage.getFirstAsync("linxColorToVtexColor", { eq: [{"linxColorCode" : colorReference}] });
if (Object.keys(linxColorToVtexColor).length === 0 || 
    linxColorToVtexColor.linxColorCode !== colorReference) { 
      throw `Color info not found in Dynamic Storage for Linx color code ${colorReference}`;
      return;
}
```

## Optional dynamic storage key
```
if (
    Object.keys(productColorRichInfo).length !== 0 &&
    "customColorName" in productColorRichInfo &&
    productColorRichInfo.customColorName &&
    "customColorNameF" in productColorRichInfo &&
    productColorRichInfo.customColorNameF
)
```
