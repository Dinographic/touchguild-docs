# ListItemNoteTypes

| Properties | Description                                                        | Type                                                                                                                                     |
| ---------- | ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| createdAt  | Timestamp of the note's creation.                                  | Number                                                                                                                                   |
| createdBy  | ID of the note's owner.                                            | String                                                                                                                                   |
| updatedAt? | Timestamp of when the note has been updated, if updated.           | Number                                                                                                                                   |
| updatedBy? | ID of the user that updated the note if the note has been updated. | String                                                                                                                                   |
| mentions?  | Mentions included in the list item note                            | <mark style="color:purple;"></mark>[<mark style="color:purple;">MentionsType</mark>](mentionstype.md)<mark style="color:purple;"></mark> |
| content    | List item note content                                             | String                                                                                                                                   |
