# Maestro Course — Mobile Testing

Repository for the **ShopDemo** application used in the mobile testing course with Maestro.

## Udemy Course

[**Maestro: Mobile Testing from Zero to Pipeline**](https://www.udemy.com/course/maestro-testes-mobile-do-zero-ao-pipeline/?referralCode=2E88CCA77E66DFD8ED4F)

A practical, hands-on course taught entirely in Portuguese, designed for QA engineers and developers who want to automate Android application testing without writing programming code, using declarative YAML flows with Maestro.

The course is built around a single real-world application, ShopDemo, and covers:

- **Environment Setup and Configuration:** Android Studio, Android Virtual Device (AVD), Java, Maestro CLI, and ADB on Windows.
- **Maestro Fundamentals:** How Maestro interacts with applications, Maestro Studio, YAML structure, relational selectors, assertions, scrolling, gestures, and wait mechanisms.
- **Building the ShopDemo Test Suite from Scratch:** Login with `clearState`, product catalog navigation, product details, shopping cart, checkout, and a complete end-to-end (E2E) flow from login to order confirmation.
- **Professional Test Organization:** Folder structure, reusable subflows with `runFlow`, environment variables, and debugging failed flows.
- **CI/CD Integration:** Running the test suite through Maestro CLI, version control with Git and GitHub, and a complete GitHub Actions pipeline with test reports and execution artifacts.
- **AI-Powered Test Automation:** Using Maestro MCP with Claude Code to generate and maintain automated tests from descriptions written in Portuguese.

By the end of the course, students will have a complete, well-organized test suite integrated into a CI pipeline, supported by an AI-assisted maintenance workflow.

## APK Download

[**ShopDemo.apk**](https://github.com/jefersoncaye/curso-maestro-testes-mobile/raw/refs/heads/master/ShopDemo.apk) — Android 7.0+ · arm64 · ~44 MB

> **Installation:** Transfer the APK file to your Android device and open it. You may need to enable **"Install apps from unknown sources"** in your Android security settings.

---

## Project Structure

The application source code is located in the [`/shopdemo`](./shopdemo) directory.

```text
shopdemo/
├── App.tsx              # Entry point and navigation
├── src/
│   ├── screens/         # Login, Catalogo, Detalhe, Carrinho, Checkout, Confirmacao
│   ├── context/         # CartContext (global shopping cart state)
│   ├── components/      # ProdutoCard, BotaoPrimario
│   └── data/            # produtos.ts (14 static products)
```

### Running Locally

```bash
cd shopdemo
npm install
npx expo start --android
```

**Prerequisites:** A running Android emulator or a physical Android device connected via ADB.

### Building a New APK

```bash
cd shopdemo/android
./gradlew assembleRelease
```

The generated APK will be available at:

```text
android/app/build/outputs/apk/release/app-release.apk
```