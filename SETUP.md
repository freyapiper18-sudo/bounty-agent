# Setup checklist — finish before 1 October

1. **Create a bot GitHub account.**
   - Use a name like `freya-bounty-bot`.
   - GitHub allows one free "machine account" per person, and you remain responsible for it.
   - Use its noreply email for commits.
2. **Connect Algora.**
   - Sign in to Algora with the bot account.
   - Complete payout onboarding now, because it involves identity checks that count as human setup.
3. **Create a public repo under the bot account.**
   - Add the files from this folder.
   - Public repos get free Actions minutes, and the log is useful for your presentation.
4. **Create a GitHub token for the bot.**
   - Go to Settings → Developer settings → Personal access tokens (classic).
   - Give it the `public_repo` scope only.
   - Save it as the repo secret `BOT_GITHUB_TOKEN`.
5. **Create a Claude token.**
   - On your own machine, with Claude Code logged in to your subscription, run `claude setup-token`.
   - Save the result as the repo secret `CLAUDE_CODE_OAUTH_TOKEN`.
6. **Add repo variables.**
   - `BOT_NAME`: the bot's username.
   - `BOT_EMAIL`: the bot's noreply email.
7. **Dry run.**
   - Go to Actions → Bounty agent → Run workflow, with dry_run ticked.
   - Check `log.md` to see that it found sensible bounties and would have submitted something reasonable.
   - Adjust `CLAUDE.md` if needed.
8. **Hands off from 1 October.**
   - To stop the agent, commit a file named `STOP` or disable the workflow.
9. **On 1 November:** revoke both tokens.
