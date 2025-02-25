The Lookup is a UI component that allows an end user to search for an item in a collection shown in a drop-down menu.

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Lookup/Basics/"
}

The following code adds the Lookup UI component to your page. The simplest configuration requires only a [dataSource](/api-reference/10%20UI%20Components/DataExpressionMixin/1%20Configuration/dataSource.md '/Documentation/ApiReference/UI_Components/dxLookup/Configuration/#dataSource') to be specified. In addition, you can define the [placeholder](/api-reference/10%20UI%20Components/dxLookup/1%20Configuration/placeholder.md '/Documentation/ApiReference/UI_Components/dxLookup/Configuration/#placeholder') to be displayed when the Lookup input field is empty.

---
##### jQuery

    <!--HTML-->
    <div id="lookupContainer"></div>

    <!--JavaScript-->
    $(function() {
        $("#lookupContainer").dxLookup({
            dataSource: [
                "HD Video Player",
                "SuperHD Video Player",
                "SuperPlasma 50",
                // ...
            ],
            placeholder: "Select a product..."
        });
    });

##### Angular

    <!--HTML-->
    <dx-lookup
        [dataSource]="lookupDataSource"
        placeholder="Select a product...">
    </dx-lookup>

    <!--TypeScript-->
    import { DxLookupModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        lookupDataSource = [ "HD Video Player", "SuperHD Video Player", "SuperPlasma 50" ];
    }
    @NgModule({
        imports: [
            // ...
            DxLookupModule
        ],
        // ...
    })

##### Vue

    <template>
        <DxLookup
            :data-source="dataSource"
            placeholder="Select a product..."
        />
    </template>

    <script>
    import 'devextreme/dist/css/dx.light.css';

    import { DxLookup } from 'devextreme-vue/lookup';

    export default {
        components: {
            DxLookup
        },
        data() {
            return {
                dataSource: [
                    'HD Video Player',
                    'SuperHD Video Player',
                    'SuperPlasma 50',
                    // ...
                ]
            };
        }
    }
    </script>

##### React

    import React from 'react';
    import 'devextreme/dist/css/dx.light.css';

    import { Lookup } from 'devextreme-react/lookup';

    const dataSource = [
        'HD Video Player',
        'SuperHD Video Player',
        'SuperPlasma 50',
        // ...
    ];

    class App extends React.Component {
        render() {
            return (
                <Lookup
                    dataSource={dataSource}
                    placeholder="Select a product..."
                />
            );
        }
    }

    export default App;

---

If your data is an array of objects, specify: 

- [valueExpr](/api-reference/10%20UI%20Components/DataExpressionMixin/1%20Configuration/valueExpr.md '/Documentation/ApiReference/UI_Components/dxLookup/Configuration/#valueExpr')     
    The data field whose value will be written into the [value](/api-reference/10%20UI%20Components/dxDropDownList/1%20Configuration/value.md '/Documentation/ApiReference/UI_Components/dxLookup/Configuration/#value') property.
- [displayExpr](/api-reference/10%20UI%20Components/DataExpressionMixin/1%20Configuration/displayExpr.md '/Documentation/ApiReference/UI_Components/dxLookup/Configuration/#displayExpr')     
    The data field whose value will be displayed within the inner [List](/concepts/05%20UI%20Components/List/00%20Getting%20Started%20with%20List '/Documentation/Guide/UI_Components/List/Getting_Started_with_List') UI component and in the input field of the Lookup.

<!---->

---
##### jQuery

    <!--JavaScript-->
    const lookupData = [
        { id: 1, country: "Afghanistan" },
        { id: 2, country: "Albania" },
        // ...
    ];

    $(function() {
        $("#lookupContainer").dxLookup({
            dataSource: lookupData,
            valueExpr: 'id',
            displayExpr: 'country'
        });
    });

##### Angular

    <!--HTML-->
    <dx-lookup
        [dataSource]="lookupDataSource"
        valueExpr="id"
        displayExpr="country">
    </dx-lookup>

    <!--TypeScript-->
    import { DxLookupModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        lookupDataSource = [
            { id: 1, country: "Afghanistan" },
            { id: 2, country: "Albania" },
            // ...
        ];
    }
    @NgModule({
        imports: [
            // ...
            DxLookupModule
        ],
        // ...
    })

##### Vue

    <template>
        <DxLookup
            :data-source="lookupData"
            value-expr="id"
            display-expr="country"
        />
    </template>

    <script>
    import 'devextreme/dist/css/dx.light.css';

    import { DxLookup } from 'devextreme-vue/lookup';

    export default {
        components: {
            DxLookup
        },
        data() {
            return {
                lookupData: [
                    { id: 1, country: 'Afghanistan' },
                    { id: 2, country: 'Albania' },
                    // ...
                ]
            };
        }
    }
    </script>

##### React

    import React from 'react';
    import 'devextreme/dist/css/dx.light.css';

    import { Lookup } from 'devextreme-react/lookup';

    const lookupData = [
        { id: 1, country: 'Afghanistan' },
        { id: 2, country: 'Albania' },
        // ...
    ];

    class App extends React.Component {
        render() {
            return (
                <Lookup
                    dataSource={lookupData}
                    valueExpr="id"
                    displayExpr="country"
                />
            );
        }
    }

    export default App;

---

#####See Also#####
#include common-link-configurewidget
- [Lookup - Configure Search Parameters](/concepts/05%20UI%20Components/Lookup/05%20Configure%20Search%20Parameters.md '/Documentation/Guide/UI_Components/Lookup/Configure_Search_Parameters/')
- [Lookup - Enable Grouping](/concepts/05%20UI%20Components/Lookup/10%20Enable%20Grouping.md '/Documentation/Guide/UI_Components/Lookup/Enable_Grouping/')
- [Lookup - Enable Paging](/concepts/05%20UI%20Components/Lookup/15%20Enable%20Paging.md '/Documentation/Guide/UI_Components/Lookup/Enable_Paging/')
- [Lookup - Customize the Appearance](/concepts/05%20UI%20Components/Lookup/20%20Customize%20the%20Appearance/05%20Customize%20Item%20Appearance.md '/Documentation/Guide/UI_Components/Lookup/Customize_the_Appearance/')
- [Lookup - Handle the Value Change Event](/concepts/05%20UI%20Components/Lookup/25%20Handle%20the%20Value%20Change%20Event.md '/Documentation/Guide/UI_Components/Lookup/Handle_the_Value_Change_Event/')
- [Lookup API Reference](/api-reference/10%20UI%20Components/dxLookup '/Documentation/ApiReference/UI_Components/dxLookup/')
- [Lookup vs SelectBox](/concepts/05%20UI%20Components/Lookup/35%20Lookup%20vs%20SelectBox.md '/Documentation/Guide/UI_Components/Lookup/Lookup_vs_SelectBox/')

[tags]dxlookup, lookup, overview, data source, value, display expression, displayExpr, valueExpr