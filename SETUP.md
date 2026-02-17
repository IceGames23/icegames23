# GitHub Profile README Setup Guide

This guide will help you set up and customize your professional GitHub profile README.

## 🎯 WakaTime Integration Setup

To enable WakaTime stats in your profile README:

### 1. Get Your WakaTime API Key
1. Sign up or log in to [WakaTime](https://wakatime.com)
2. Go to [Settings → API Key](https://wakatime.com/settings/api-key)
3. Copy your API key

### 2. Add WakaTime Secret to GitHub
1. Go to your profile repository: `https://github.com/IceGames23/icegames23`
2. Navigate to **Settings** → **Secrets and variables** → **Actions**
3. Click **New repository secret**
4. Name: `WAKATIME_API_KEY`
5. Value: Paste your WakaTime API key
6. Click **Add secret**

### 3. Create GitHub Actions Workflow
Create `.github/workflows/waka-readme.yml`:

```yaml
name: Waka Readme

on:
  schedule:
    # Runs at 00:00 UTC every day
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  update-readme:
    name: Update this repo's README
    runs-on: ubuntu-latest
    steps:
      - uses: athul/waka-readme@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
```

### 4. Trigger the Workflow
1. Go to **Actions** tab in your repository
2. Select **Waka Readme** workflow
3. Click **Run workflow** → **Run workflow**
4. Wait for it to complete (usually takes 1-2 minutes)

Your WakaTime stats will now appear in the README and update daily!

## 🎨 Customization Options

### Change Theme
The README uses the `tokyonight` theme. You can change it to:
- `dark`, `radical`, `merko`, `gruvbox`, `tokyonight`, `onedark`, `cobalt`, `synthwave`, `highcontrast`, `dracula`

Just replace `theme=tokyonight` in the URLs with your preferred theme.

### Add More Badges
Visit [shields.io](https://shields.io) to create custom badges for:
- Social media profiles
- Programming languages
- Certifications
- Technologies you use

### Update Discord Link
Replace `https://discord.gg/your-invite-link` with your actual Discord server invite link.

### Add More Stats
Check out these resources:
- [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats)
- [GitHub Readme Streak Stats](https://github.com/DenverCoder1/github-readme-streak-stats)
- [Activity Graph](https://github.com/Ashutosh00710/github-readme-activity-graph)

## 📝 Content Updates

### Update Projects
As you create new repositories:
1. Add them to the **Featured Projects** section
2. Update star counts
3. Add brief descriptions

### Update Skills
Add new technologies and tools as you learn them in the **Technologies & Tools** section.

### Update About Me
Keep your bio current with:
- Current projects you're working on
- Technologies you're learning
- Your interests and goals

## 🔄 Regular Maintenance

- **Monthly**: Review and update project descriptions and star counts
- **Quarterly**: Update skills and technologies
- **As needed**: Update contact information and links

## 🎉 Tips for an Awesome Profile

1. **Be authentic**: Share your genuine interests and skills
2. **Keep it updated**: Regular updates show you're active
3. **Showcase your best work**: Pin your best repositories
4. **Be concise**: Keep descriptions short and impactful
5. **Use emojis wisely**: They add personality but don't overdo it

## 📚 Additional Resources

- [Awesome GitHub Profile README](https://github.com/abhisheknaiidu/awesome-github-profile-readme)
- [GitHub Profile README Generator](https://rahuldkjain.github.io/gh-profile-readme-generator/)
- [Shields.io Badge Generator](https://shields.io)
- [Simple Icons](https://simpleicons.org) for more logo options

---

**Need help?** Open an issue in this repository or reach out on Discord!
