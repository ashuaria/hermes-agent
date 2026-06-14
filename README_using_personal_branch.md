# Using the `personal/ashuaria` Branch on Another Server

This branch is a personal fork of Hermes Agent with custom patches applied
(e.g., the setup-wizard fix that respects the user's choice to decline the
`/v1` suffix).

## One-time setup on the other server

```bash
git clone https://github.com/ashuaria/hermes-agent.git
cd hermes-agent
git checkout personal/ashuaria
./setup-hermes.sh
```

`setup-hermes.sh` installs the venv, editable package, and CLI symlink.
After it finishes, `hermes` is ready to use with your patched code.

## Keeping in sync

```bash
cd hermes-agent
git fetch origin
git rebase origin/main personal/ashuaria
git checkout personal/ashuaria
```
