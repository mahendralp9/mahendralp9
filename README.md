### Hi there 👋

<!--
**mahendralp9/mahendralp9** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<!--START_SECTION:waka-->
<!--END_SECTION:waka-->

name: Waka Readme

on:
  workflow_dispatch: # for manual workflow trigger
  schedule:
    - cron: "0 0 * * *" # runs at every 12AM UTC

jobs:
  update-readme:
    name: WakaReadme DevMetrics
    runs-on: ubuntu-latest
    steps:
      - uses: athul/waka-readme@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          # following flags are required, only if this is not on
          # profile readme, remove the leading `#` to use them
          #GH_TOKEN: ${{ secrets.GH_TOKEN }}
          #REPOSITORY: <gh_username/gh_username>
