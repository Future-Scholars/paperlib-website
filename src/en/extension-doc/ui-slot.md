# UI Slots

In this article, we will introduce the UI slots that can be used and modified in Paperlib.

## Slot in the Paper Details Panel

In the Paper Details Panel, we have three slots:

- `paperDetailsPanelSlot1`: Under the publication date of the paper.
- `paperDetailsPanelSlot2`: Under the rating of the paper.
- `paperDetailsPanelSlot3`: Under the supplementary materials of the paper.

## Slot in the Notification View

In the Notification View, we have one slot:

- `overlayNotifications`: The notification that appears on the top of the screen.

To show the content in the slot, you need to update the overlay `overlayNoticationShown = true`:

```typescript
PLAPI.uiStateService.setState({"overlayNoticationShown": true});
```

### Slot Content

```typescript
{
    title: string,
    content: string
}
```

### Update Slot

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

`id` is the unique identifier of the content. If the `id` is already in the slot, the content will be updated. Otherwise, a new content will be added.