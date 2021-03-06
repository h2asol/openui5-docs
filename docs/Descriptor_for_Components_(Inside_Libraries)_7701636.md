<!-- loio7701636d088147569d99b4f08d418bd9 -->

| loio |
| -----|
| 7701636d088147569d99b4f08d418bd9 |

<div id="loio">

view on: [demo kit nightly build](https://openui5nightly.hana.ondemand.com/#/topic/7701636d088147569d99b4f08d418bd9) | [demo kit latest release](https://openui5.hana.ondemand.com/#/topic/7701636d088147569d99b4f08d418bd9)</div>

## Descriptor for Components \(Inside Libraries\)

The descriptor for components contains a subset of the attributes in the descriptor for applications

Attributes in the `sap.app` namespace<a name="loio7701636d088147569d99b4f08d418bd9__table_rpm_xjz_45"/>

|Attribute|Comment|
|---------|-------|
| `id` |Mandatory|
| `type` |With value `component`; mandatory|
| `i18n` |Optional attribute: A URL string to the properties file that contains the text symbols for the descriptor; the URL is interpreted relative to the `manifest`. Alternatively, an object defined as described in [Terminologies](Terminologies_eba8d25.md). If the manifest contains placeholders in `{{...}}` syntax but no `i18n` attribute has been provided, the default value `i18n/i18n.properties` is used to request a ResourceBundle.|
| `embeddedBy` |Mandatory, for example, `"../"` |
| `title` |Mandatory|
| `subTitle` | |
| `description` | |
| `ach` | |
| `dataSources` | |
| `cdsViews` | |
| `resources` |Mandatory; must have value `resources.json` as file; it is generated by the library build with this name|
| `offline` | |
| `sourceTemplate` | |

Attributes in the `sap.ui` namespace<a name="loio7701636d088147569d99b4f08d418bd9__table_sry_dlz_45"/>

|Attribute|Comment|
|---------|-------|
| `technology` |With value `UI5`; mandatory|
| `deviceTypes` | |
| `supportedThemes` | |

Attributes in the `sap.ui5` namespace<a name="loio7701636d088147569d99b4f08d418bd9__table_ydc_bmz_45"/>

|Attribute|Comment|
|---------|-------|
| `resources` | |
| `dependencies` | `libs` `components` |
| `models` | |
| `rootView` | |
| `handleValidation` | |
| `config` | |
| `routing` | |
| `extends` | `component` `minVersion` |
| `contentDensities` | |
| `componentName` | |

Attributes in the `sap.mobile` namespace<a name="loio7701636d088147569d99b4f08d418bd9__table_o1x_lmz_45"/>

|Attribute|Comment|
|---------|-------|
| `definingRequests` | |

***

### Library Name Determination

SAPUI5 determines the library name by analyzing the component namespace \(package\) up to the part where the segment starts with a capitalized letter. If the library name that has been determined, does not fit your component, an additional library attribute needs to be filled in the component metadata in `Component.js` to specify the library your component belongs to.

Example:

``` js

sap.ui.core.UIComponent.extend("com.sap.fancylibrary.sub.CompLib.Component", {
    metadata : {
        "manifest" : "json",
        "library" : "com.sap.fancylibrary",
    ...
}
```

