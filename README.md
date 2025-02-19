# ESist
Repositório relativo ao grupo 13 de Engenharia de Sistemas, "Radar Processing (RP) for DVB-RAD Project". \

GIT STRUCTURE:
  -   MAIN (BRANCH): Stable. No direct commits here. \
  -   Develop: The integration branch where all features are merged before going to main. \
  -   Feature: temporary branch for merging with develop \

## **📌 Branch Structure**
- `main` → **Stable, production-ready code** (no direct commits)
- `develop` → **Integration branch** (features merge here before `main`)
- `feature/*` → **Feature branches** (each new feature gets its own branch)
---

## **📌 Workflow for Contributing**

### **1️⃣ Start from `develop`**
```sh
git checkout develop
git pull origin develop  # Ensure you have the latest code
```

### **2️⃣ Create a Feature Branch**
```sh
git checkout -b feature/<feature-name>
```

### **3️⃣ Work on the Feature**
```sh
git add .
git commit -m "Add feature: <short description>"
```

### **4️⃣ Push the Feature Branch to Remote**
```sh
git push origin feature/<feature-name>
```

### **5️⃣ Open a Pull Request (PR)**
- **Target branch:** `develop`
- **Request review** from at least **1 other developer**
- **Resolve conflicts if needed**
- **Wait for approval before merging**

#### 🔥 **Before Merging: Rebase Your Feature Branch** *(Keeps history clean)*
```sh
git checkout develop
git pull origin develop  # Get the latest updates
git checkout feature/<feature-name>
git rebase develop  # Move feature branch on top of latest develop
```
- If conflicts arise, **resolve them** and run:
  ```sh
  git add .
  git rebase --continue
  ```
- If you mess up, **abort rebase**:
  ```sh
  git rebase --abort
  ```
- Push the rebased branch (**force-with-lease to avoid overwriting others' work**):
  ```sh
  git push --force-with-lease origin feature/<feature-name>
  ```

### **6️⃣ After the PR is Merged**
```sh
git checkout develop  # Move back to develop
git pull origin develop  # Sync with latest changes
git branch -d feature/<feature-name>  # Delete local feature branch
git push origin --delete feature/<feature-name>  # Delete remote feature branch
```

