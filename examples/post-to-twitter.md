# Example: Post to Twitter

## Your Prompt

```
Post this to Twitter:

"Most founders spend 2 hours a day on social media.

I spend 30 seconds.

The difference? I talk to my AI agent and it handles the rest.

Setup: Claude Code + Late MCP + 3 custom Skills.

The entire system is free. Link in bio."
```

## What Claude Does

1. Reads the `late-social-media` skill
2. Prepares the post content
3. Shows you the post for confirmation:
   ```
   Platform: Twitter
   Content: [your text]
   Ready to post?
   ```
4. You say "yes"
5. Claude posts via Late API
6. Returns the post URL

## Result

Your tweet is live. Total time: ~15 seconds.
