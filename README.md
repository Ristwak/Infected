# INFECTED — TECHNICAL REVIEW REPORT

**Project:** Infected  
**Engine:** Unreal Engine 5  
**Genre:** First-Person Shooter / Zombie Fighting  
**Review Type:** Unreal Engine Project Structure and Technical Configuration Review  
**Repository:** Ristwak/Infected  
**Review Scope:** Project Structure, Configuration, Asset Organization, Build Artifacts and Project Distribution

---

## 1. Project Overview

Infected is a zombie-fighting First-Person Shooter (FPS) game developed using Unreal Engine 5.

The project is designed around a zombie combat experience and is distributed through Google Drive because of its large project size.

The externally hosted project directory contains the Unreal Engine project file and several standard Unreal Engine directories, including Content, Config, DerivedDataCache, Intermediate and Saved.

This review focuses on the visible project structure, organization and technical distribution setup.

---

## 2. Project Structure

The provided Google Drive screenshot shows the following project files and directories:

### Root Directory

- `.git` — Git version-control metadata.
- `Config` — Unreal Engine project configuration files.
- `Content` — Main project content directory for game assets and resources.
- `DerivedDataCache` — Generated asset-processing cache.
- `Intermediate` — Intermediate files generated during project processing and builds.
- `Saved` — Generated project data, logs and saved information.
- `.gitattributes.txt` — Git-related attribute configuration file.
- `ZombieGame.uproject` — Main Unreal Engine project descriptor.
- `East_SPG_2S3Akatsia.png` — Image asset.
- `West_AA_Patriot.png` — Image asset.
- `West_Command_M1130.png` — Image asset.
- `West_Radar_Patriot.png` — Image asset.
- `West_Truck_M923.png` — Image asset.

The directory follows the general structure of an Unreal Engine project.

---

## 3. Unreal Engine Project Configuration

**Primary File:** `ZombieGame.uproject`

The project descriptor is present in the root directory.

The `Config` directory is also available and provides the expected location for project configuration files.

These are important components for opening and managing an Unreal Engine project.

**Technical Verification Limitations:**

- The exact Unreal Engine version has not been verified.
- Project plugin dependencies have not been inspected.
- Input mappings and gameplay configuration have not been inspected.
- Rendering and scalability settings have not been verified.
- Build and packaging configuration has not been inspected.

---

## 4. Content and Asset Organization

**Primary Directory:** `Content`

The Content directory is present in the shared project folder.

It is the primary location for Unreal Engine assets, including Blueprints, meshes, materials, textures, animations, audio and levels.

However, the internal directory structure and individual assets have not been inspected.

The project also includes several PNG files related to military vehicles or equipment, visible in the root directory.

### Recommendations

- Organize assets into clearly named folders.
- Separate gameplay Blueprints from environment and character assets.
- Keep materials, textures, meshes and animations organized.
- Use consistent naming conventions.
- Avoid unnecessary duplicate assets.
- Keep project-specific assets separate from third-party resources where practical.

---

## 5. Generated Files and Project Management

The shared directory includes:

- DerivedDataCache
- Intermediate
- Saved

These directories contain generated or locally produced project data.

### Technical Observations

- DerivedDataCache stores generated asset-processing data.
- Intermediate contains generated intermediate files.
- Saved may contain logs, autosaves and other generated project data.

These directories can increase the size of a shared project archive.

For project distribution, it is worth evaluating whether generated files need to be included in the shared package.

A clean project distribution should retain the required project configuration, content and dependencies while avoiding unnecessary generated data.

---

## 6. Project Distribution and Version Control

The project is hosted externally on Google Drive rather than directly inside GitHub.

This approach is understandable for a project with a reported size of approximately 7–8 GB.

The GitHub repository provides a separate reference to the externally hosted project.

### Recommendations

- Maintain a clear project download link.
- Document the required Unreal Engine version.
- Include setup and extraction instructions.
- Provide a list of required plugins and dependencies.
- Consider using Git LFS or another suitable large-file distribution solution where appropriate.
- Maintain a clear distinction between source assets and generated project files.

---

## 7. Performance and Optimization Review Scope

The visible directory structure alone does not establish the runtime performance of the game.

The following areas require inspection of the actual Unreal Engine project:

1. Texture resolutions and texture streaming settings.
2. Static and skeletal mesh complexity.
3. Material and shader complexity.
4. Level composition and actor counts.
5. Lighting and shadow configuration.
6. Blueprint execution and tick usage.
7. AI navigation and enemy behaviour.
8. Animation performance.
9. Memory usage and asset loading.
10. Build size and packaging configuration.

No runtime performance problems have been confirmed from the available screenshots.

---

## 8. Recommended Improvements

1. Document the exact Unreal Engine version.
2. Review and document project plugin dependencies.
3. Maintain a clear Content directory hierarchy.
4. Evaluate the inclusion of generated directories in project distribution.
5. Add project setup and execution instructions.
6. Document asset naming and organization conventions.
7. Verify project configuration and packaging settings.
8. Perform runtime profiling before making performance claims.

---

## 9. Overall Assessment

Infected is distributed as an Unreal Engine project rather than only a gameplay demonstration.

The visible project directory contains the main `.uproject` descriptor, configuration directory, content directory and standard generated project directories.

The project distribution approach uses Google Drive to accommodate its reported large file size.

The main areas identified for further technical evaluation are project configuration, asset organization, dependency management, generated-file handling and runtime optimization.

A complete gameplay and implementation review requires inspection of the internal Content directory, including Blueprints, levels, assets and any available source code.

**Review Scope:** This assessment is based on the supplied Google Drive screenshots and visible project directory structure. Internal Blueprint logic, C++ implementation, gameplay systems, asset quality, project configuration contents and runtime performance have not been independently inspected or tested.
