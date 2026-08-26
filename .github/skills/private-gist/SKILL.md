---
name: private-gist
description: Creates non-public GitHub gists for notes, canvas snippets, or samples when the user asks to save or share session material.
license: MIT
---

# Private gist

Create gists only with GitHub's non-public setting. GitHub calls these
**secret gists**: they are unlisted, not access-controlled, and anyone with the
URL can read them. Explain this distinction before creation.

## Workflow

1. Ask what material belongs in the gist and whether an unlisted link provides
   sufficient privacy. Recommend a private repository instead when true access
   control is required.
2. Draft the description, filenames, and exact content locally or in the chat.
3. Remove credentials, tokens, personal data, customer data, proprietary
   source, and other sensitive content. Do not assume unlisted means secure.
4. Show the complete proposed gist to the user and obtain explicit approval
   before the external write.
5. Use an available authenticated GitHub tool. Set `public` to `false` when
   using the API, or use `gh gist create --private` when the GitHub CLI is the
   approved available tool. Never use public visibility, even if requested
   later in the same task.
6. Verify the created gist is marked secret/non-public before returning its
   URL. If visibility cannot be verified, report that and do not describe the
   gist as private.

Never place authentication tokens in commands, files, logs, or chat. Do not
silently create, update, or delete a gist.
