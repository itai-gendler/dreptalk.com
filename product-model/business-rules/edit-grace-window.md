---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "edit-post"
    },
    {
      "type": "entity",
      "id": "post-version"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/forum/editPolicy.ts#EDIT_GRACE_MS"
    }
  ]
}
---

# Edits within fifteen minutes of posting are silent

An edit within fifteen minutes of posting replaces the text with no marker. After that, every edit keeps the earlier text as a version and marks the post edited. Engagement does not end the window early.
