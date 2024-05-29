# ReferenceService

## Call

```typescript
import { PLAPI } from "paperlib-api/api";

PLAPI.referenceService.methodname(...);
```

## Avaliable Methods

### `replacePublication`

```typescript
/**
 * Abbreviate the publication name according to the abbreviation list set in the preference interface.
 * @param source - The source paper entity.
 * @returns The paper entity with publication name abbreviated.
 */
replacePublication(source: PaperEntity): PaperEntity;
```

### `toCite`

```typescript
/**
 * Convert paper entity to citationjs object.
 * @param source - The source paper entity.
 * @returns The cite object.
 */
toCite(source: PaperEntity | PaperEntity[] | string): any;
```

### `exportBibTexKey`

```typescript
/**
 * Export BibTex key.
 * @param paperEntities - The paper entities.
 * @returns The BibTex key.
 */
exportBibTexKey(paperEntities: PaperEntity[]): string;
```

### `exportBibTexBody`

```typescript
/**
 * Export BibTex body string.
 * @param paperEntities - The paper entities.
 * @returns The BibTex body string.
 */
exportBibTexBody(paperEntities: PaperEntity[]): string;
```

### `exportBibTex`

```typescript
/**
 * Export plain text.
 * @param paperEntities - The paper entities.
 * @returns The plain text.
 */
exportPlainText(paperEntities: PaperEntity[]): Promise<string>;
```

### `exportCSV`
```typescript
/**
 * Export papers as csv string.
 * @param paperEntities - The paper entities.
 * @returns The CSV string.
 */
exportCSV(paperEntities: PaperEntity[]): Promise<string>;
```

### `exportBibTexKeyInFolder`
```typescript
/**
 * Export BibTex body string in folder.
 * @param folderName - The folder name.
 */
exportBibTexBodyInFolder(folderName: string): Promise<string>;
```

### `exportBibTexBodyInFolder`
```typescript
/**
 * Export plain text in folder.
 * @param folderName - The folder name.
 */
exportPlainTextInFolder(folderName: string): Promise<string>;
```

### `exportBibItem`
```typescript
/**
 * Export BibItem.
 * @param paperEntities - The paper entities.
 * @returns The BibItem.
 */
exportBibItem(paperEntities: PaperEntity[]): Promise<string>;
```


### `export`

```typescript
/**
 * Export paper entities.
 * @param paperEntities - The paper entities.
 * @param format - The export format: "BibTex" | "BibTex-Key" | "PlainText"
 */
export(paperEntities: PaperEntity[], format: string): Promise<void>;
```