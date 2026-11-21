# Radiophos Issue Triage & Roadmap

*Generated from 26 open issues in `jaqbj/RadiophosApp` (private repo)*

---

## Summary by Priority

| Priority | Count | Issues |
|----------|-------|--------|
| **Urgent** | 3 | #30 (docs), #28 (landscape mode), #2 (CarPlay) |
| **High** | 8 | #42, #41, #40, #39, #37, #36, #35, #34 (iOS/macOS bugs) |
| **Medium** | 10 | #44, #43, #31, #29, #26, #24, #14, #13, #4, #2 (features) |
| **Low** | 5 | #38, #25, #23, #33, #32 |

---

## Categorized Issues

### 🔴 URGENT — Blockers for 1.0 Release

| # | Title | Platform | Type | Notes |
|---|-------|----------|------|-------|
| **30** | Finalise documentation for the project | All | Documentation | Assigned to jaqbj; Urgent priority; needed for public release |
| **28** | Modular landscape mode for tablets and phones | iOS, iPadOS, Android | Feature | Urgent priority; seasonal scenes (Christmas/Halloween), config-driven; scenes already exist in Shared/Scenes |
| **2** | Apple Car (iOS) | iOS | Feature | 2 comments; needs Apple entitlement; Car mode (`e1419de`) is stopgap; deprioritized 2026-11-13 |

---

### 🟠 HIGH — Critical Bugs (iOS/macOS Playback & TLS)

| # | Title | Platform | Type | Root Cause / Notes |
|---|-------|----------|------|-------------------|
| **42** | Removing AirPods stops playing, doesn't resume on reinsert | iOS | Bug | Audio session interruption handling; play/pause in app doesn't resume |
| **41** | Alarm plays → radio stops, doesn't resume; play does nothing | iOS | Bug | Audio session category/interruption; needs stop+play to recover |
| **40** | Sleep button has 1-minute test option | iOS | Bug | UI bug in sleep timer picker |
| **39** | Night mode doesn't dim when player view selected | iOS | Bug | Theme/appearance not applying in Now Playing |
| **37** | iOS PreRelease performance — TLS errors, stuttering | iOS | Bug | `WRONG_VERSION_NUMBER` (TLS 1.3 vs server), connection drops, `nw_endpoint_flow_failed` |
| **36** | PreRelease Log fresh build iOS (stuttering) | iOS | Bug | Same TLS/connection issues as #37; `boringssl_context_handle_fatal_alert` |
| **35** | Pre Release MacOS build logs v1.0 (5) | macOS | Bug | Layout recursion, TLS errors, `FigFilePlayer` errors, `CRABS` signals |
| **34** | Error messages MacOS — DNS/connection failures | macOS | Bug | `nw_endpoint_flow_failed`, DNS resolution failure for `fi1.api.radio-browser.info` |

**Common theme**: TLS/connection issues (#37, #36, #35, #34) — Radio Browser API endpoints failing, wrong TLS version, connection drops. Likely needs:
- TLS configuration review (minimum TLS version, cipher suites)
- Retry/fallback logic for Radio Browser mirrors
- Better error handling & user-facing messages

**Audio session issues** (#42, #41) — Need proper `AVAudioSession` interruption handling, route change observers.

---

### 🟡 MEDIUM — Features & Enhancements

| # | Title | Platform | Type | Effort | Notes |
|---|-------|----------|------|--------|-------|
| **44** | 1.1: Bottom bar reorder (station name first) | macOS, Windows, Linux | Feature | Low | Windows/Linux: `NowPlayingBar.dart`; macOS: `NowPlayingTicker.swift`; phones unchanged |
| **43** | Redesign Settings Tab | iOS, iPadOS, Android | Feature | Medium | Mobile-only; current Setup is embedded dialog |
| **31** | Add visualization option (Orbit view) | All | Feature | Medium | Globe rotation + Sun/Moon + "you are here"; `maxiVisual` setting; issue #31 in CLAUDE.md |
| **29** | Linux port | Linux | Feature | High | Flatpak + tar.gz; Flutter supports Linux; porting started |
| **26** | Some stations (Soma Deep Space One) lose visualization | iOS, iPadOS | Bug/Feature | Low | Visualization stops after few seconds; may be format-specific (HLS/Opus) |
| **24** | Save track metadata as ID3 tags in recordings | All | Feature | Medium | Provenance tags decided 2026-11-14 (ID3v2.3); MP3/AAC done; extend to track info |
| **14** | Filter duplicate stations (keep best quality) | All | Feature | Medium | Mobile UI de-cramping; Radio Browser returns multiple streams per station |
| **13** | Stream buffer + live catch-up | All | Feature | High | 5-min buffer on pause, "Catch Up"/"Live" button; pre-capture in feature requests |
| **4** | Design skin system instead of themes | All | Feature | High | Reserved `.skin` folders in Shared/README.md; asset support not built; deprioritized for v2 |

---

### 🟢 LOW — Nice to Have

| # | Title | Platform | Type | Notes |
|---|-------|----------|------|-------|
| **38** | Jellyfin/Plex library access | iOS, iPadOS, Android | Feature | Priority: Low, Effort: High; like PlexD |
| **25** | Screen saver mode (fullscreen after inactivity) | macOS, Windows | Feature | Priority: Low; muted radio, favorite station, key bindings |
| **23** | Full screen mode (visualization focus) | macOS, Windows, Linux | Feature | Visualization main stage, station info, weather, time |
| **33** | macOS font weight warning (Segoe UI) | macOS | Bug | SwiftUI warning; font not installed; fallback needed |
| **32** | Multiple macOS font weight errors | macOS | Bug | Same as #33; Segoe UI not on macOS |

---

## Recommended Roadmap

### Phase 1: 1.0 Release Blockers (Week 1-2)
1. **#30** — Finalize documentation (public repo sync, release notes, privacy)
2. **#28** — Modular landscape mode (scenes exist, need wiring on iOS/Android)
3. **#42, #41** — Audio session interruption handling (iOS)
4. **#40, #39** — Sleep timer & night mode UI fixes (iOS)
5. **#37, #36, #35, #34** — TLS/connection stability (Radio Browser mirrors, retry logic, TLS config)

### Phase 2: 1.1 Polish (Week 3-4)
6. **#44** — Bottom bar reorder (desktop platforms)
7. **#43** — Settings redesign (mobile)
8. **#26** — Visualization persistence for problematic stations
9. **#33, #32** — Font fallback for missing fonts (macOS)

### Phase 3: Post-1.1 Features (Month 2+)
10. **#31** — Orbit visualization (globe + astronomy)
11. **#24** — Track metadata in recording tags
12. **#14** — Duplicate station filter
13. **#29** — Linux port (Flatpak)
14. **#13** — Stream buffer + catch-up
15. **#4** — Skin system (v2)

### Phase 4: Nice to Have
16. **#2** — Real CarPlay (needs Apple entitlement)
17. **#38** — Jellyfin/Plex integration
18. **#25, #23** — Screensaver/fullscreen modes

---

## Platform-Specific Focus

### iOS/iPadOS (Most Critical Bugs)
- **Audio session**: #42, #41, #40, #39
- **TLS/Network**: #37, #36
- **UI**: #27, #26
- **Features**: #43, #28

### macOS
- **TLS/Network**: #35, #34
- **Fonts**: #33, #32
- **UI**: #44 (ticker), #8 (genre buttons wrap — done per CLAUDE.md)

### Windows/Android/Linux (Flutter)
- **Feature parity**: #44, #29, #28
- **Visualizations**: Working per CLAUDE.md (Phase 2 step 5b done)

---

## Dependencies & Blockers

| Issue | Blocks | Blocked By |
|-------|--------|------------|
| #37/#36 (TLS) | All iOS network features | Radio Browser API stability |
| #28 (Landscape) | Scenes UX | #31 (Orbit) optional |
| #29 (Linux) | Flatpak packaging | Flutter Linux stable |
| #2 (CarPlay) | Real CarPlay | Apple entitlement approval |
| #4 (Skins) | Asset pipeline | Theme system stable |

---

## Labels Applied

| Label | Applied to Issues |
|-------|------------------|
| `tls-network` | #37, #36, #35, #34 |
| `audio-session` | #42, #41 |
| `release-blocker` | #30, #28, #2 |
| `mobile-ui` | #43, #27, #26, #40, #39 |
| `desktop-ui` | #44, #33, #32 |

---

## Milestones (Create Manually)

**1.0 Release** (due 2026-12-15): #30, #28, #2, #42, #41, #40, #39, #37, #36, #35, #34
**1.1 Polish** (due 2027-01-15): #44, #43, #26, #33, #32
**2.0 Features** (no due date): #31, #24, #14, #29, #13, #4

---

## Next Steps

1. **Create milestones** via GitHub UI or `gh` CLI
2. **Assign issues** to milestones
3. **Begin Phase 1 implementation** with Claude Code
4. **Sync documentation** to public `Radiophos.App` repo (#30)

---

*This triage is based on issue content, labels, custom fields (Priority/Effort), and CLAUDE.md status notes.*