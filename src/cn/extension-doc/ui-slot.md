# UI 插槽

本文介绍了 Paperlib 中提供的可以使用，修改的 UI 插槽。

## 论文详情面板插槽

在论文的详情面板，我提供三个插槽：

- `paperDetailsPanelSlot1`: 在论文发表时间之下。
- `paperDetailsPanelSlot2`: 在论文的评分之下。
- `paperDetailsPanelSlot3`: 在论文的补充材料之下。

## 通知视图插槽

在通知视图中，我提供一个插槽：

- `overlayNotifications`: 出现在屏幕顶部的通知。

要在插槽中显示内容，您需要更新 `overlayNoticationShown = true`：

```typescript
PLAPI.uiStateService.setState({"overlayNoticationShown": true});
```

### 插槽内容

```typescript
{
    title: string,
    content: string
}
```

### 插槽更新

```typescript
PLAPI.uiSlotService.updateSlot(
    "paperDetailsPanelSlot1", 
    {
        [id: string]: {
            title: string,
            content: string
        }
    }
);

```

`id` 是内容的唯一标识符。如果 `id` 已经在插槽中，内容将被更新。否则，将添加新内容。