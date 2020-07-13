# How to add information about new card

First of all, thank you for thinking about adding information about new card.

To add info about new card you need to create PR with file `new/new.json`.

Here is the minumum valid content of that file:

```json
{
    "name" : "%NAME%",
    "site" : "%SITE%",
    "status" : "%STATUS%"
}
```

But you need to put real data into that file:

 * `%NAME%` — the name of the card. It is the string that is used when when the card is added to Home Assistant UI (`- type: 'custom:animated-consumption-card'`) but without `custom:`
 * `%SITE%` — the card url. Usually it is link to GitHub repo, e.g. `https://github.com/bessarabov/animated-consumption-card`
 * `%STATUS%` — it can `active` or `deprecated`. Status `deprecated` should be used only when there is information in thre repositorey that this project is deprecated and/or the GitHub repo is archived. If there is no such info in the repo the status stays `active`, even if there is no recent commits.

## `card_id`

For the new card you don't have to specify `card_id`. It will be generated.

## Additional info

You can also add field "repo", but it is not required. It can be added only for the cards that are stored at GitHub repo and there is only one UI card in that repo.

```json
{
    "name" : "%NAME%",
    "repo" : {
        "clone_url" : "%CLONE_URL%",
        "type" : "github"
    },
    "site" : "%SITE%",
    "status" : "%STATUS%"
}
```

 *  `%CLONE_URL%` — This is a direct url that can be used in `git clone` command. It should be https url, not git url.

## Adding image

Adding image is optinal. Images are not stored in this repo. So to add image to the card, you need to attach image to the Pull Requst.
Image will be taken from that PR, uploaded and added to the card info.
