# Nibiaa Edge: Customization Plan

This document tracks the strategic transformation of ThingsBoard CE into the Nibiaa Edge platform.

## 🏁 Phase 1: Visual Identity & Rebranding
**Goal**: Establish the "Nibiaa" look across the entire UI.
- [ ] Update `appTitle` in `environment.ts`
- [ ] Modify `$tb-primary-color` and `$tb-secondary-color` in `constants.scss`
- [ ] Replace `logo_white.svg` and `logo_title_white.svg`
- [ ] Bulk replace "ThingsBoard" text in `locale.constant-en_US.json`
- [ ] Replace `favicon.ico`

## 🎨 Phase 2: UI/UX Enhancements
**Goal**: Tailor the user experience for Nibiaa customers.
- [ ] Customize Login Page background and styles
- [ ] Reconfigure Sidebar menu items
- [ ] Create custom default Dashboard templates

## ⚙️ Phase 3: Backend & Rule Engine
**Goal**: Support unique IoT hardware and logic.
- [ ] Implement custom Java Rule Nodes
- [ ] Configure `thingsboard.yml` for Nibiaa defaults
- [ ] Set up global branding environment variables

## 🚀 Phase 4: Production Packaging
**Goal**: Reliable builds and deployment.
- [ ] Automate UI + Backend Docker builds
- [ ] Configure custom Docker registry push
- [ ] Verify Edge-to-Cloud synchronization

---

## 🛠 Build Instructions
To rebuild after changes:
1. `mvn clean install -DskipTests -pl ui-ngx`
2. `mvn clean install -DskipTests -pl msa/web-ui -P push-docker-image`
3. `docker-compose up -d --force-recreate tb-web-ui1`
