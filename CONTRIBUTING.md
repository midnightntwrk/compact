# Contributing

We welcome your contributions to the Midnight network! By contributing, you'll play a vital role in shaping the future of a blockchain focused on data privacy.

## Getting Started

This repository is only used to host Compact releases.
If you would like to report a Compact bug, make a feature request, get the source code, etc.
then you should go to the Minokawa project's [Compact repository](https://github.com/LFDT-Minokawa/compact).

## Developer Certificate of Origin (DCO)

All contributions must include a sign-off in every commit message, certifying that you have the right to submit the code under the project license. This is done by adding a `Signed-off-by` trailer using `git commit -s`:

```
git commit -s -m "feat: your commit message"
```

This produces a commit message like:

```
feat: your commit message

Signed-off-by: Your Name <your@email.com>
```

By signing off, you agree to the [Developer Certificate of Origin (version 1.1)](https://developercertificate.org/).

If you have forgotten to sign off past commits in a PR, you can amend them:

```bash
# Amend the last commit
git commit --amend -s --no-edit

# Or rebase to sign off multiple commits (replace N with the number of commits)
git rebase --signoff HEAD~N
```

A DCO GitHub App runs on every pull request and will block merges until all commits are signed off.

### Automating sign-off

To avoid having to remember `-s` on every commit, install a `prepare-commit-msg` hook in your clone of this repo that appends the sign-off automatically:

```bash
cat > .git/hooks/prepare-commit-msg <<'EOF'
#!/bin/sh
NAME=$(git config user.name)
EMAIL=$(git config user.email)
grep -qs "^Signed-off-by: " "$1" || printf "\nSigned-off-by: %s <%s>\n" "$NAME" "$EMAIL" >> "$1"
EOF
chmod +x .git/hooks/prepare-commit-msg
```

After installing the hook, every `git commit` in this repo will include a `Signed-off-by` trailer automatically. Make sure your `user.name` and `user.email` are set correctly, since the hook certifies the DCO on your behalf for every commit.

## Support and Communication:

Ask anything about Midnight! We're here to help. Connect with us on [Discord](https://discord.com/invite/midnightnetwork), [Telegram](https://t.me/Midnight_Network_Official), and [X](https://x.com/MidnightNtwrk) and Join the Community to stay updated and engage with other Midnight enthusiasts.

We appreciate your contributions!
