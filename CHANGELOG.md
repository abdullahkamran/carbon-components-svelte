# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

<!-- ## Unreleased -->

## [0.21.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.21.0) - 2020-10-26

**Features**

- ListBoxMenu: forward "scroll" event ([PR #366](https://github.com/IBM/carbon-components-svelte/pull/366))
- ComboBox: export reference to list box menu ([PR #366](https://github.com/IBM/carbon-components-svelte/pull/366))
- DataTable: add `ToolbarMenu`, `ToolbarMenuItem` ([PR #369](https://github.com/IBM/carbon-components-svelte/pull/369))
- DataTable: support empty table body columns by adding optional `empty` key to `headers` prop ([PR #370](https://github.com/IBM/carbon-components-svelte/pull/370))
- Dropdown: support "sm", "xl" field sizes

**Fixes**

- DataTable: cancelling batch selection should deselect "select all rows" checkbox
- Toolbar: remove duplicate "bx--toolbar-content" element

**Documentation**

- DataTable: add example ["Empty column with overflow menu"](https://carbon-svelte.vercel.app/components/DataTable#empty-column-with-overflow-menu)
- hand off current theme for examples opened in a new tab
- add field size examples for `Dropdown`, `MultiSelect`, `Select`

## [0.20.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.20.0) - 2020-10-24

**Features**

- DataTable: add `Toolbar`, `ToolbarContent`, `ToolbarSearch`, `ToolbarBatchActions`
- DataTable: support row selection, batch selection, radio selection
- DataTable: dispatch "mouseenter", "mouseleave" events on table rows
- Search: forward "focus", "blur" events to search input; dispatch "clear" event

**Fixes**

- DataTable: include sort direction with custom sort method ([PR #356](https://github.com/IBM/carbon-components-svelte/pull/356))
- fix: allow item ids in ComboBox, Dropdown, MultiSelect to be numbers
- fix(ui-shell): initialize `platformName` as empty string to prevent rendering as "undefined"

**Refactoring**

- refactor(ui-shell): remove redundant conditional in HeaderGlobalAction

**Documentation**

- new DataTable examples:
  - [With custom display and sort methods](https://carbon-svelte.vercel.app/components/DataTable#with-custom-display-and-sort-methods)
  - [With toolbar](https://carbon-svelte.vercel.app/components/DataTable#with-toolbar)
  - [With toolbar (small size)](https://carbon-svelte.vercel.app/components/DataTable#with-toolbar-small-size)
  - [Selectable](https://carbon-svelte.vercel.app/components/DataTable#selectable)
  - [Initial selected rows](https://carbon-svelte.vercel.app/components/DataTable#initial-selected-rows)
  - [Selectable with batch actions](https://carbon-svelte.vercel.app/components/DataTable#selectable-with-batch-actions)
  - [Selectable (radio)](https://carbon-svelte.vercel.app/components/DataTable#selectable-radio)
- fix(docgen): list both default and named slots in `COMPONENT_INDEX.md`

## [0.19.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.19.0) - 2020-10-23

**Features**

- DataTable: add optional display and sort methods in header object ([PR #352](https://github.com/IBM/carbon-components-svelte/pull/352))
- ProgressIndicator: add preventChangeOnClick; default value is `false` ([PR #351](https://github.com/IBM/carbon-components-svelte/pull/351))
- TooltipDefinition: make tooltip text slottable through `slot="tooltip"`

**Fixes**

- ProgressIndicator: make `currentIndex` reactive ([PR #351](https://github.com/IBM/carbon-components-svelte/pull/351))
- ComposedModal: use `onDestroy` for destroy logic due to async usage of `onMount`([PR #348](https://github.com/IBM/carbon-components-svelte/pull/348))
- Search: forward `size` prop to Search skeleton

**Refactoring**

- TooltipDefinition: remove redundant `hidden` reactive variable

**Breaking Changes**

- ProgressIndicator: clicking a completed step will update `currentIndex`; to opt out of this default behavior, set `preventChangeOnClick` to `true`

**Documentation**

- ContentSwitcher: add "Selected index" example
- CodeSnippet: add multi-line skeleton example
- InlineLoading: add UX example showcasing various statuses

## [0.18.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.18.0) - 2020-10-17

**Features**

- DataTable: support individual, batch row expansion ([PR 341](https://github.com/IBM/carbon-components-svelte/pull/341))
- DataTable: make header, row cells slottable ([PR 342](https://github.com/IBM/carbon-components-svelte/pull/342))

**Fixes**

- fix(data-table): fix misaligned tall row table headers ([PR 340](https://github.com/IBM/carbon-components-svelte/pull/340))
- Documentation generator: parse `ArrayExpression` in exported props ([PR 341](https://github.com/IBM/carbon-components-svelte/pull/341))

**Breaking Changes**

- Remove top-level slot in `DataTable` in favor of named slots ([PR 341](https://github.com/IBM/carbon-components-svelte/pull/341))

**Documentation**

- add Component API metadata ([PR 340](https://github.com/IBM/carbon-components-svelte/pull/340))
- DataTable: add expandable, batch expandable examples ([PR 341](https://github.com/IBM/carbon-components-svelte/pull/341))
- DataTable: add slottable cells example ([PR 342](https://github.com/IBM/carbon-components-svelte/pull/342))

## [0.17.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.17.0) - 2020-10-16

**Features**

- feat: set `rel="nooopener noreferrer"` if `target="_blank"` on link components ([PR #321](https://github.com/IBM/carbon-components-svelte/pull/321))
- feat: support `Search` disabled state ([PR #330](https://github.com/IBM/carbon-components-svelte/pull/330))
- feat(button-skeleton): add size prop consistent with Button ([PR #332](https://github.com/IBM/carbon-components-svelte/pull/332))
- feat(progress-indicator-skeleton): add count prop ([PR #332](https://github.com/IBM/carbon-components-svelte/pull/332))
- feat(accordion): add disabled prop for `Accordion` and `AccordionItem` ([PR #333](https://github.com/IBM/carbon-components-svelte/pull/333))
- feat(accordion): add "sm", "xl" size variants to `Accordion` and `AccordionSkeleton` ([PR #333](https://github.com/IBM/carbon-components-svelte/pull/333))
- feat(content-switcher): add "sm", "xl" size variants ([PR #334](https://github.com/IBM/carbon-components-svelte/pull/334))
- feat(code-snippet): add wrapText prop for "multi" type CodeSnippet ([PR #335](https://github.com/IBM/carbon-components-svelte/pull/335))
- feat(aspect-ratio): add AspectRatio component ([PR #336](https://github.com/IBM/carbon-components-svelte/pull/336))
- feat(dropdown): dispatch select event, use window instead of body for click events ([PR #339](https://github.com/IBM/carbon-components-svelte/pull/339))

**Fixes**

- fix(combo-box): disabled combobox should not open ([PR #329](https://github.com/IBM/carbon-components-svelte/pull/329))
- fix(inline-loading): add wrapper class "bx--inline-loading" ([PR #332](https://github.com/IBM/carbon-components-svelte/pull/332))
- fix(breadcrumb): forward noTrailingSlash to skeleton ([PR #332](https://github.com/IBM/carbon-components-svelte/pull/332))
- fix(skeleton-text): unkey paragraph rows due to high collision rate ([PR #332](https://github.com/IBM/carbon-components-svelte/pull/332))
- fix(accordion-skeleton): forward align prop ([PR #333](https://github.com/IBM/carbon-components-svelte/pull/333))

**Refactoring**

- refactor(icon): remove old logic that inferred icon size from function name ([PR #332](https://github.com/IBM/carbon-components-svelte/pull/332))

**Documentation**

- AspectRatio (new component): demo all ratios
- Breadcrumb: use `noTrailingSlash` in skeleton example
- Button: demo skeleton size variants
- CodeSnippet: add example "Wrap text"
- ComboBox: add examples "Light variant," "Filterable"
- ContentSwitcher: add examples "Extra-large size" and "Small size"
- SkeletonText: add example "Paragraph with custom line count"
- Pagination: add example "Hidden page size"
- ProgressIndicator: demo custom step count for skeleton
- Link: add example `Target _blank`
- MultiSelect: add example "No alphabetical sorting"
- Accordion: add examples for "Extra-large" and "Small" size variants
- Accordion: add examples for "Disabled" and "Disabled (item)"
- AccordionSkeleton: add examples "Skeleton (chevron aligned left)" and size variants

**Housekeeping**

- chore(deps-dev): bump carbon-components to ^v10.22 ([PR #337](https://github.com/IBM/carbon-components-svelte/pull/337))
- retire Storybook by removing Storybook-related dependencies, set-up and stories ([PR #331](https://github.com/IBM/carbon-components-svelte/pull/331))
- use `npm-run-all` to run `build:css` and `build:lib` in parallel ([PR #331](https://github.com/IBM/carbon-components-svelte/pull/331))

## [0.16.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.16.0) - 2020-10-12

**Features**

- Pagination: add `pageSizeInputDisabled` prop to hide page size buttons (default is `false`) ([PR #292](https://github.com/IBM/carbon-components-svelte/pull/292))
- ListBoxMenu: add `ref` prop ([PR #303](https://github.com/IBM/carbon-components-svelte/pull/303))
- Pre-compiled CSS: upgrade `carbon-components` to version 10.21

**Fixes**

- Link: explicitly define `href` prop to fix TypeScript errors ([PR #301](https://github.com/IBM/carbon-components-svelte/pull/301))
- RadioButtonGroup: explicitly define `id` prop to fix TypeScript errors ([PR #303](https://github.com/IBM/carbon-components-svelte/pull/303))
- ComboBox: `light` prop should use the light variant ([PR #303](https://github.com/IBM/carbon-components-svelte/pull/303))
- ComposedModal: class "bx--body--with-modal-open" should be removed when closing the modal ([PR #306](https://github.com/IBM/carbon-components-svelte/pull/306))
- Dropdown: remove unused `setContext` import ([PR #308](https://github.com/IBM/carbon-components-svelte/pull/308))
- `css/all.css`: default theme should be "white," not "g10" ([PR #322](https://github.com/IBM/carbon-components-svelte/pull/322))
- UI Shell: `HeaderAction` menu should close when clicking in the window, not just the document body ([PR #323](https://github.com/IBM/carbon-components-svelte/pull/323))

**Performance**

- DatePicker: remove default i10n locales import to reduce bundle size by ~42 kB ([PR #316](https://github.com/IBM/carbon-components-svelte/pull/316))

**Breaking Changes**

- DatePicker: default i10n locales are no longer imported
- if using `css/all.css`, set the "theme" attribute on the HTML element to "g10" in order to use the Gray 10 theme

**Documentation**

- Redesign component documentation website (Short link: [ibm.biz/carbon-svelte](http://ibm.biz/carbon-svelte)); deployments sponsored by Vercel
- Update development workflow in `CONTRIBUTING.md`
- Typo fixes in `README.md` ([PR #324](https://github.com/IBM/carbon-components-svelte/pull/324), [PR #325](https://github.com/IBM/carbon-components-svelte/pull/325))

**Housekeeping**

- Git hooks: only lint staged files in the pre-commit Git hook ([PR #319](https://github.com/IBM/carbon-components-svelte/pull/319))

## [0.15.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.15.0) - 2020-10-01

**Features**

- DataTableSkeleton: add `size` prop to support "compact", "small", "tall" row heights ([PR #279](https://github.com/IBM/carbon-components-svelte/pull/279), thanks [@albertms10](https://github.com/albertms10))

- HeaderPanelLink: forward click event ([PR #286](https://github.com/IBM/carbon-components-svelte/pull/286), thanks [@weaseldotro](https://github.com/weaseldotro))

- FluidForm: add `FluidForm` component and support fluid variants for `TextInput`, `PasswordInput` ([PR #293](https://github.com/IBM/carbon-components-svelte/pull/293), thanks [@josefaidt](https://github.com/josefaidt))

- UI Shell: add `ref` prop to interactive (i.e. anchor links, buttons) UI Shell elements ([PR #297](https://github.com/IBM/carbon-components-svelte/pull/297), thanks [@josefaidt](https://github.com/josefaidt))

**Fixes**

- Slider: attach mousemove/touch events to document body, not slider input ([issue #288](https://github.com/IBM/carbon-components-svelte/issues/288))

- Slider: `value` prop type should be a `number`, not a `string` ([issue #289](https://github.com/IBM/carbon-components-svelte/issues/289))

- Slider: input value should not update if `disabled` is `true`

- Slider: `change` event should only be dispatched if the value changes

- UI Shell: correctly bind `ref` prop in `HeaderGlobalAction` ([PR #297](https://github.com/IBM/carbon-components-svelte/pull/297), thanks [@josefaidt](https://github.com/josefaidt))

- export `DatePickerSkeleton`, `FileUploaderSkeleton` components

**Breaking Changes**

- DataTableSkeleton: `compact` prop is removed in favor of `size="compact"`

**Dependencies**

- upgrade `carbon-icons-svelte` to version ^10.17.0

**Housekeeping**

- prettier: enable `svelteBracketNewLine` for improved readability ([PR #281](https://github.com/IBM/carbon-components-svelte/pull/281), thanks [@josefaidt](https://github.com/josefaidt))

- git: add husky, lint-staged to development workflow ([PR #295](https://github.com/IBM/carbon-components-svelte/pull/295), thanks [@josefaidt](https://github.com/josefaidt))

## [0.14.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.14.0) - 2020-09-23

**Features**

- `Modal`, `ComposedModal`: add `preventCloseOnClickOutside` prop
- `Modal`: add `alert` prop to support alertdialog ARIA role ([PR #273](https://github.com/IBM/carbon-components-svelte/pull/273), thanks [@josefaidt](https://github.com/josefaidt))
- `TextInput`: add `warn` prop ([PR #275](https://github.com/IBM/carbon-components-svelte/pull/275), thanks [@josefaidt](https://github.com/josefaidt))
- `TextInput`: add `inline` prop ([PR #277](https://github.com/IBM/carbon-components-svelte/pull/277), thanks [@josefaidt](https://github.com/josefaidt))

**Fixes**

- `DataTableSkeleton`: add `showHeader`, `showToolbar` props
- `OverflowMenu`: focus menu button on escape key only
- `DataTable`: fix `headers` JSDoc type annotation ([PR #271](https://github.com/IBM/carbon-components-svelte/pull/271), thanks [@albertms10](https://github.com/albertms10))

**Breaking Changes**

- `DataTableSkeleton`: `showHeader` and `showToolbar` are `true` by default

## [0.13.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.13.0) - 2020-09-18

**Features**

- Move helper text below form inputs in `ComboBox`, `Dropdown`, `MultiSelect`, `TextArea`, `NumberInput`, `TextInput`, `Select` ([PR #256](https://github.com/IBM/carbon-components-svelte/pull/256), [issue #255](https://github.com/IBM/carbon-components-svelte/issues/255))

- ProgressIndicator: add `spaceEqual` prop and functionality ([PR #263](https://github.com/IBM/carbon-components-svelte/pull/263), [issue #262](https://github.com/IBM/carbon-components-svelte/issues/262))

**Fixes**

- Link: remove visited styles by default ([PR #259](https://github.com/IBM/carbon-components-svelte/pull/259), [issue #258](https://github.com/IBM/carbon-components-svelte/issues/258))

- TimePickerSelect: deprecate `hideLabel` prop to match spec and set default value to `true` ([PR #261](https://github.com/IBM/carbon-components-svelte/pull/261), [issue #260](https://github.com/IBM/carbon-components-svelte/issues/260))

**Breaking Changes**

- TimePickerSelect: `hideLabel` prop is `true` by default

## [0.12.3](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.12.3) - 2020-09-16

**Fixes**

- ClickableTile: add missing `href` ([PR #254](https://github.com/IBM/carbon-components-svelte/pull/254), thanks [@josefaidt](https://github.com/josefaidt))

## [0.12.2](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.12.2) - 2020-09-14

**Fixes**

- Dropdown: allow event propagation when clicking the chevron icon (73861e2)

## [0.12.1](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.12.1) - 2020-09-14

**Fixes**

- Pagination: ensure `page`, `pageSize` values are numbers (0138910)
- Pagination: dispatch "update" event only when `pageSize` or `page` values update (458d1b5)
- Pagination: use correct size carbon icons for buttons (size `16` instead of `24`) (192f98d)
- ProgressStep: use button element; set negative `tabindex` if `disabled` is `true` (3202f39)
- ProgressStep: forward click event (6cb877e)
- SideNavMenu, SideNavMenuItem: remove "role", "aria-haspopup" attributes causing a11y warnings
- RadioTile: move `keydown`, `tabindex` to input element (17d97d1)

## [0.12.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.12.0) - 2020-09-13

**Features**

- css: ship precompiled CSS StyleSheets for each Carbon theme (70e0875)

**Documentation**

- examples: add example set-ups using popular bundlers/frameworks
- update README guidance on consuming the library

## [0.11.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.11.0) - 2020-09-05

**Features**

- UI Shell: add `HeaderGlobalAction` component (7b3c111)

## [0.10.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.10.0) - 2020-09-05

**Features**

- UI Shell: add Close/AppSwitcher as default icons for `HeaderAction` component (5f62cde)
- ButtonSet: add `stacked` prop (c8e0a59)
- Link: set `rel` attribute to "noopener noreferrer" if `target` is "\_blank" (4b7d254)

**Fixes**

- TextInput: add missing `required` prop to input (PR #237), thanks [@kamil-murtaza](https://github.com/kamil-murtaza))
- StructuredList: change element semantics from `section` to `div` to avoid accessibility error (117dbcf)
- MultiSelect: add `light` variant to text input (6a955b1)
- NumberInput: disable label, helper text if `disabled` is set to `true` (37c7f07)
- Pagination: use singular page range text if `total` is 1 (3d64fb2)

**Housekeeping**

- add `.prettierrc` and enable `svelteStrictMode` (42b8159)
- remove documentation of non-existent `small` Button prop (41a533d)
- upgrade TypeScript to version >=4 (e7e67f3)
- bump prettier, prettier-plugin-svelte (322b238)
- bump rollup, rollup plugins (00b9068)
- require node >=12 for development/CI (bf0f11a)

## [0.9.7](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.9.7) - 2020-08-23

- Fix `InlineNotification` and `ToastNotification` timeout
  ([PR#235](https://github.com/IBM/carbon-components-svelte/pull/235), thanks [@Overbryd](https://github.com/Overbryd))

## [0.9.6](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.9.6) - 2020-08-15

- use svelte compiler to generate TypeScript definitions, documentation (issue #227, PR #228)
- fix `DatePicker` to use default imports (reverts 6d5f1e5; issue #232)

## [0.9.5](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.9.5) - 2020-08-12

- fix `Modal` and `ComposedModal` to prevent modal from closing unexpectedly ([PR #231](https://github.com/IBM/carbon-components-svelte/pull/231))

## [0.9.4](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.9.4) - 2020-08-08

- ignore false positive `a11y-label-has-associated-control` warnings added in svelte^v3.24.1
- fix `DatePicker`: use wildcard import to resolve flatpickr "no default" error when using ESM
- allow `CodeSnippet` button to be optional by using the `hideCopyButton` prop
- refactor `CodeSnippet`: replace afterUpdate with reactive statement
- fix `CodeSnippet`: forward `feedback`, `feedbackTimeout` props to `Copy` component

## [0.9.3](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.9.3) - 2020-08-02

- rename UI Shell `Header` slot from "skip-to-main-content" to "skip-to-content"
- support fixed `SideNav`
- add `expandedByDefault` prop to `Header` to prevent `SideNav` from being expanded

## [0.9.2](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.9.2) - 2020-08-01

- add "skip-to-main-content" slot to `Header`
- make `platformName` prop in UI Shell `Header` slottable (i.e. <span slot="platform">...</span>)
- make `company` prop `Header` optional
- fix UI Shell `Header` to add space between company and platform name for ARIA label
- fix UI Shell `HeaderAction` bug where panel would not open
- add `ButtonSet` component
- fix `Accordion` to avoid `$$restProps.class` override

## [0.9.1](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.9.1) - 2020-07-30

- fix `TabContent` to remove hidden prop when panel is selected

## [0.9.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.9.0) - 2020-07-30

- add TypeScript definitions
- dispatch "select" and "clear" events in `ComboBox`
- forward `keydown` event to `TextInput`, `PasswordInput` components
- add `count` prop to `TabsSkeleton`
- apply toggle behavior to `HeaderAction` button; dispatch "open" and "close" events
- fix forwarded click event in `CodeSnippet`
- fix class name typo in `UnorderedList`

## [0.8.5](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.8.5) - 2020-07-23

- add `noGutter`, `noGutterLeft`, `noGutterRight` props to `Grid`, `Row`, `Column`
- add `aspectRatio` prop to `Column`

## [0.8.4](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.8.4) - 2020-07-22

- add Grid components (`Grid`, `Row`, `Column`)
- add `PaginationNav` component
- fix `TooltipIcon` to avoid `$$restProps.class` override

## [0.8.3](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.8.3) - 2020-07-20

- bump `carbon-icons-svelte` dependency to version >=10.14.0
- support `size` prop (`undefined` or `"sm"` or `"lg`) in `DatePickerInput`, `NumberInput`, `Select`, `PasswordInput`, `TextInput` components
- support light variant for `ContentSwitcher`
- focus `ComboBox` after clearing the selection
- fix `ListBox` regression where size class can be overriden by `$$restProps.class`
- fix `Pagination` regression where current page selection value is stuck at `1`

## [0.8.2](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.8.2) - 2020-07-19

- fix `ComboBox` to close dropdown menu when pressing the "Escape" key ([Issue #198](https://github.com/IBM/carbon-components-svelte/issues/198))

## [0.8.1](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.8.1) - 2020-07-19

- fix bug in `Tag` to prevent custom class from overriding tag class
- fix SSR rendering issue in `Modal` by replacing `onDestroy` with `onMount` ([Issue #200](https://github.com/IBM/carbon-components-svelte/issues/200))

## [0.8.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.8.0) - 2020-07-19

- use \$\$restProps API (requires Svelte version >=3.20)
- upgrade `carbon-icons-svelte` to version >=10.13.0
- use svelte class:{value} API instead of `cx`
- add ref prop to "interactive" components like text inputs, anchor links... ([Issue #196](https://github.com/IBM/carbon-components-svelte/issues/196))
- add slot to Content Switcher `Switch` component ([Issue #183](https://github.com/IBM/carbon-components-svelte/issues/183))
- fix `ContentSwitcher` bug where bound `selectedIndex` could not be updated
- remove unused lib utilities (cx, css, fillArray)
- refactor component exports and folder structure
- create Sapper app for e2e testing and alternative development environment in `docs/`
- update Travis CI config to build library, build storybook, and run e2e tests in `docs/`
- remove Jest in favor of integration/e2e testing with Cypress
- update contributing guidelines

## [0.7.6](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.7.6) - 2020-07-19

- Add named slot to UI Shell `HeaderAction` component for text
  ([PR#201](https://github.com/IBM/carbon-components-svelte/pull/201), thanks [@danielboven](https://github.com/danielboven))

## [0.7.5](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.7.5) - 2020-07-17

- Add `name` prop to form-related components
  ([PR#199](https://github.com/IBM/carbon-components-svelte/pull/199), thanks [@softartisan](https://github.com/softartisan))

- Add `Content`, `SkipToContent` components to the UI Shell

- Forward `on:click` event to UI Shell `Header` component

## [0.7.4](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.7.4) - 2020-06-17

- Fix `OverflowMenu` focus behavior to set `didOpen` only if `open` is true ([PR#193](https://github.com/IBM/carbon-components-svelte/pull/193))

## [0.7.3](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.7.3) - 2020-06-16

- Fix `OverflowMenu` to focus button only after closing the menu ([PR#192](https://github.com/IBM/carbon-components-svelte/pull/192))

## [0.7.2](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.7.2) - 2020-06-04

- Add sort direction to dispatched "click:header" event for a sortable `DataTable`
  ([PR#188](https://github.com/IBM/carbon-components-svelte/pull/188), thanks [@mabentley85](https://github.com/mabentley85)!)

## [0.7.1](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.7.1) - 2020-06-03

- Add missing RadioTile export

## [0.7.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.7.0) - 2020-05-29

- Dispatch "update" event in `Pagination` for `pageSize`, `page` variables
  ([PR#185](https://github.com/IBM/carbon-components-svelte/pull/185), thanks [@mabentley85](https://github.com/mabentley85)!)

- Drop carbon-components as a peer dependency

## [0.6.3](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.6.3) - 2020-05-26

- Replace `"javascript:void(0)"` with `"/"` in `HeaderNavMenu` href attribute to fix a11y "not a valid attribute" warning; `href` is an exported property that can be overriden by the consumer
  ([Issue #184](https://github.com/IBM/carbon-components-svelte/issues/184))

- Ignore `a11y-no-onchange` warning in `TimePickerSelect`

- Bump development dependency `svelte` to v3.23.0

## [0.6.2](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.6.2) - 2020-05-09

- Fix `tileMaxHeight` bug in `ExpandableTile` by setting the value only if the default value is 0
  ([Issue #180](https://github.com/IBM/carbon-components-svelte/issues/180))

## [0.6.1](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.6.1) - 2020-05-08

- Fix `Pagination` bug by binding the correct variable (`selected`) to the `Select` component
  ([PR#179](https://github.com/IBM/carbon-components-svelte/pull/179), thanks [@ericol](https://github.com/ericol)!)

## [0.6.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.6.0) - 2020-05-07

- Fix button with icon bug by manually setting `hasIconOnly` in `Button`. This results in a breaking change for icon-only buttons, which now must include `hasIconOnly`
  ([Issue #174](https://github.com/IBM/carbon-components-svelte/issues/174))

## [0.5.1](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.5.1) - 2020-05-03

- Fix focus/dispatch bug in `Modal`, `ComposedModal`
  ([PR#173](https://github.com/IBM/carbon-components-svelte/pull/173), thanks [@mfeitoza](https://github.com/mfeitoza)!)

## [0.5.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.5.0) - 2020-04-29

- Ship `DataTable` that supports sorting

- Pin dependencies, remove commitlint, husky, eslint, prettier

## [0.4.2](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.4.2) - 2020-04-20

- Forward `on:blur` event to Select component
  ([PR#169](https://github.com/IBM/carbon-components-svelte/pull/169), thanks [@httpsOmkar](https://github.com/httpsOmkar)!)

## [0.4.1](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.4.1) - 2020-04-18

- Refactor UI Shell components to be modular (header, left panel, right panel)
  ([PR#168](https://github.com/IBM/carbon-components-svelte/pull/168), thanks [@mfeitoza](https://github.com/mfeitoza)!)

## [0.4.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.4.0) - 2020-04-18

- Refactor UI Shell to be component-based
  ([PR#166](https://github.com/IBM/carbon-components-svelte/pull/166), thanks [@mfeitoza](https://github.com/mfeitoza)!)

## [0.3.3](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.3.3) - 2020-03-09

- Fix "window is undefined" error when using UIShell with server-side rendering (SSR)
  ([PR#149](https://github.com/IBM/carbon-components-svelte/pull/149), thanks [@pbxothi](https://github.com/pbxothi)!)

## [0.3.2](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.3.2) - 2020-02-12

- Fix `SkeletonText` duplicate style attribute to work with `svelte^3.18.2`
  ([#134](https://github.com/IBM/carbon-components-svelte/issues/134))

## [0.3.1](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.3.1) - 2020-02-03

- Fix `DatePicker` locale initialization bug

- Fix `CheckboxSkeleton` styles; bump `carbon-components` version to ^10.9.3

## [0.3.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.3.0) - 2020-02-03

- Add `UIShell` component (thanks [@Heydan83](https://github.com/Heydan83)!)
  ([#10](https://github.com/IBM/carbon-components-svelte/issues/10))

- Add single component skeleton states for `Accordion`, `CodeSnippet`

- Fix `Select`, `SelectItem` to support two-way binding, programmatic prop setting

- Fix `Tab` to set `selected` prop to `currentIndex` after updating

## [0.2.1](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.2.1) - 2020-01-08

- Check if `l10n.en` is defined in `DatePicker` component to resolve Svelte REPL compilation

## [0.2.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.2.0) - 2020-01-08

- Include `src` in files published to npm to resolve Svelte module entry
  ([#102](https://github.com/IBM/carbon-components-svelte/issues/102))

- Support most Carbon components (See the [GitHub project](https://github.com/IBM/carbon-components-svelte/projects/1))

## [0.1.0](https://github.com/IBM/carbon-components-svelte/releases/tag/v0.1.0) - 2019-12-15

- Initial release
