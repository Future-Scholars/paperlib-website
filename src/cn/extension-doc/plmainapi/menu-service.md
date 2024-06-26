# MenuService

## Call

```typescript
import { PLMainAPI } from "paperlib-api/api";

PLMainAPI.menuService.methodname(...);
```

## Avaliable Methods

### `enableGlobalShortcuts`

```typescript
/**
 * Enable global shortcuts.
 */
enableGlobalShortcuts(): void;
```

### `disableGlobalShortcuts`

```typescript
/**
 * Disable global shortcuts.
 */
disableGlobalShortcuts(): void;
```

### `click`

```typescript
/**
 * Click menu item in a programmatic way.
 * @param key
 */
click(key: keyof IMenuServiceState): void;
```

## Events

| Event ID | Callback Value | Description |
| --- | --- | --- |
| `preference` | `{key: 'preference'}` | When Preference is clicked |
| `File-enter` | `{key: 'File-enter'}` | When `File-Open` is clicked in the menu bar |
| `File-copyBibTex` | `{key: 'File-copyBibTex'}` | When `File-Copy BibTex` is clicked in the menu bar |
| `File-copyBibTexKey` | `{key: 'File-copyBibTexKey'}` | When `File-Copy BibTex Key` is clicked in the menu bar |
| `Edit-rescrape` | `{key: 'Edit-rescrape'}` | When `Edit-Rescrape` is clicked in the menu bar |
| `Edit-edit` | `{key: 'Edit-edit'}` | When `Edit-Edit` is clicked in the menu bar |
| `Edit-flag` | `{key: 'Edit-flag'}` | When `Edit-Flag` is clicked in the menu bar |
| `View-preview` | `{key: 'View-preview'}` | When `View-Preview` is clicked in the menu bar |
| `View-next` | `{key: 'View-next'}` | When `View-Next` is clicked in the menu bar |
| `View-previous` | `{key: 'View-previous'}` | When `View-Previous` is clicked in the menu bar |



