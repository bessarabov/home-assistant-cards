# How to add image

It is much better when there is a screenshot of a card.

## How to create a screenshot of a card

To create a screenshot for the card you need to add it to your Home Assistant.
Then you need to create a separate view and add UI card to that view:

![](https://upload.bessarabov.ru/bessarabov/gBlTx_hXDkNjODYoQN2gyLmFReE.png)

Then you should make screenshot of the page and use some image editor to
crop the card:

![](https://upload.bessarabov.ru/bessarabov/ZM3hFaxtqtsMohg1-ZpYoizXlDc.png)

The width of the image should be 492 pixels. The height can by any number,
for different cards there are different heights.

Then you should remove rounded corders in the image editor.

And save image as a `.png` file.

Several things that help create a good screenshot:

 * The Home Assistant theme should be default
 * There should be some real data on the card
 * The screenshot should show some default usage of the card, without lot of customization
 * All the names should be in English language

## How to add screenshot to the card

This repo does not store images. So, you should not commit files with images to the git.
To add image to the existing card you need to create a New issue and add the image
to the issue. Then the images will be uploaded and added to the card metadata.

If you are adding new card ([documentataion](/docs/how_to_add_information_about_new_card.md)),
you can attach the image to the comment in PR.
