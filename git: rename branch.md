Today I had a use case when I needed to rename branch which was already pushed to github. I planned to do one stuff in the branch, but then realized that some setup was needed before actual work.

I made 2 steps:

- renamed branch in github from repo's branches page
- typed following commands in my local cli/terminal, where first name is an old one and second name is a new one

```bash
git branch -m feature/web-interface feature/setup-deps-and-liveview
git fetch origin
git branch -u origin/feature/setup-deps-and-liveview feature/setup-deps-and-liveview
git remote set-head origin -a
```
