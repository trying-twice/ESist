# ESist
Repositório relativo ao grupo 13 de Engenharia de Sistemas, "Radar Processing (RP) for DVB-RAD Project".


GIT STRUCTURE:
  -   MAIN (BRANCH): Stable. No direct commits here.
  -   Develop: The integration branch where all features are merged before going to main.
  -   Feature: temporary branch for merging with develop

Approach:\
1. Start from develop:\
   git checkout develop\
   git pull origin develop  # Ensure you have the latest code\
2. Create a Feature Branch:\
    git checkout -b feature/<feature-name>\
3. Work on the Feature:\
    git add .\
    git commit -m "Add feature: <short description>"\
5. Push the Feature Branch to Remote\
    git push origin feature/<feature-name>\
6. Open a Pull Request (PR)\
    Target branch: develop\
    Request review from at least 1 other developer.\
    Resolve conflicts if needed.\
7. After the PR is Merged\
    git checkout develop  # Move back to develop\
    git pull origin develop  # Sync with latest changes\
    git branch -d feature/<feature-name>  # Delete local feature branch\
    git push origin --delete feature/<feature-name>  # Delete remote feature branch\
