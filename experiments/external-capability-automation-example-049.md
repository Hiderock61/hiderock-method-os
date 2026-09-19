# 自動化実例049｜Plugin Management＋GitHub→Miro外付け能力・5層ゲート盤

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Pluginの状態を二値ではなく、
5層のどこで停止しているかとして可視化する。

```text
GitHub canonical status ─┐
Plugin Management ───────┼→ Miro 5-layer gate board → reREAD
Runtime exposure ────────┘
```

## 5 layers

1. Directory
2. Runtime Tool
3. Permission / Auth
4. Live Data
5. Final State

## Targets

| Plugin | Directory | Runtime | Auth/Permission | Live Data | Final |
|---|---|---|---|---|---|
| Miro | installed=true | EXPOSED | Allow all actions | board/table proven | PROVEN |
| HubSpot | installed=true | EXPOSED | default + WRITE reauth | schema READ proven | READ PROVEN / WRITE GATED |
| Railway | installed=true | EXPOSED | default / READ auth works | projects=0 | READY / NO PROJECTS |
| Convex | not returned in current search | EXPOSED | Allow all actions | no live inventory read surface | HOLD |
| MotherDuck | not returned in current search | EXPOSED | default / reconnect loop | live read not reached | HOLD |

## Miro

Table:
**外付け能力・5層ゲート盤｜Directory × Runtime × Auth × Data × PROVEN**

Widget:
https://miro.com/app/board/uXjVHnIlKBU=/?moveToWidget=3458764684303447582

## Re-read

5/5 rows matched across:
- plugin
- directory
- runtime
- auth/permission
- live data
- final state
- blockage layer

## Audit

- Directory absence is not treated as uninstall
- Runtime exposure is not treated as connection success
- ChatGPT permission is not treated as provider OAuth success
- No live data may mean empty account, not broken connector
- Final state follows canonical GitHub PROVEN / READY / HOLD records

## Proven

- GitHub index read = **PROVEN**
- Plugin Management search = **PROVEN**
- Plugin Management permission read = **PROVEN**
- Runtime exposure audit = **PROVEN**
- Miro table create/sync/read = **PROVEN**

## Boundary

No permission changes.
No install/uninstall.
No OAuth changes.
No provider reauthorization.

## Notion

https://app.notion.com/p/3e0c10ec598c8151af73dae45921d2c4?pvs=204
