# Paxi CosmWasm Game & Lottery Open-Source Template + Invisible-UX Starter Kit
## Proposal Full Details — 188,000 PAXI

> Combined scope: **Three Kingdoms Card Game** + **Choujiang (Lottery)** — both already running on Paxi.

## 1. Proposer Background

- Independent developer on Paxi.
- Paxi currently has **36 smart contracts running**. **8 of the code IDs were uploaded by the proposer** (code IDs 29–36, verifiable on-chain), including:
  - Three Kingdoms Card Game core contracts (cw721 NFT, staking/reward, PvP settlement)
  - Lottery / raffle contract (including a single-token "danbi" edition)
- Both games are production-ready and run normally on Paxi.
- Game URL: `<your-game-url>`
- Representative contract addresses:
  - 三国 cw721 (NFT): `<paxi1...>`
  - 三国 staking/reward: `<paxi1...>`
  - 三国 PvP settlement: `<paxi1...>`
  - choujiang lottery (danbi edition): `<paxi1...>`
- The remaining 28 contracts on Paxi were deployed by other teams; this proposal does **not** claim contribution to them.
- Current on-chain activity is early: the lottery contract has completed **dozens of real interactions**; the game contracts have been **upgraded 4 times**. User base is still small.
- Early feedback from a small group of holders and existing players has been incorporated into scope and budget. This proposal does not claim broad community support.

## 2. The Gap

Paxi has 36 contracts running, but:

- No public, reusable CosmWasm **game** template (Three Kingdoms card game family).
- No public, reusable CosmWasm **lottery / raffle** template (incl. single-token edition).
- No public integration guide or reference frontend covering both.
- No public reference pattern for "invisible blockchain UX".
- New developers and players face a high entry barrier, while existing activity remains early.

This proposal funds extracting **two validated contract families** (game + lottery) into reusable MIT templates — not new contract development from scratch.

## 3. Deliverables

1. MIT repo planned under Paxi Ecosystem org: `cosmwasm-game-template`
   - `contracts/game/` — parameterized 三国 cw721, staking, PvP settlement
   - `contracts/lottery/` — parameterized choujiang lottery (incl. single-token "danbi" edition)
   - `frontend-demo/` — React demo covering both game and lottery flows
   - `docs/` — README, architecture, integration guide, FAQ
   - `scripts/` — deploy & testnet scripts
2. cw721-base compatible traits and hardcode parameterization for both families.
3. Testnet deployment with verifiable contract addresses + 2-week monitoring for **both** game and lottery contracts.
4. Reference React frontend demo.
5. Invisible-UX starter kit (optional module):
   - wallet abstraction, gas relay / paymaster example, tx status sync
   - trust-boundary documentation (who pays gas, what users authorize, session key / custody boundaries, exit path)
   - contract layer remains on-chain verifiable
6. Documentation: README, architecture, integration guide, deploy scripts, React demo startup, FAQ. Optional 5-minute screen recording; no professional video production.
7. Three months of maintenance for the open-source template repo and examples.
8. Testnet lottery experience event:
   - community members try the lottery demo on testnet
   - testnet tokens have no value; no mainnet PAXI rewards; non-investment and non-gambling
   - target at least **100 testnet interactions** (target, not a hard guarantee)
9. Public build log: weekly updates on GitHub / forum with progress, testnet addresses, and screenshots.

## 4. Budget (188,000 PAXI, ~3.05% of 6,168,000 PAXI DAO pool)

| Item | PAXI |
|------|------|
| Engineering: 三国 + choujiang 合约清理、参数化、cw721-base 适配、基础 React demo、无感 UX 示例 | 120,000 |
| Testnet 部署 + QA + 抽奖体验活动 + 2 周监控（两游戏） | 28,000 |
| Docs + 集成指南 + FAQ（无专业视频） | 20,000 |
| 3 个月模板维护 | 20,000 |
| **Total** | **188,000** |

Rationale: combined scope covers two validated contract families (card game + lottery incl. single-token edition), multi-week engineering, two testnet deployments, documentation, a testnet experience event, and three months of scoped maintenance. At current prices 188,000 PAXI has low fiat value — a small public-good investment, not a large treasury request. Engineering is the largest line because the core deliverable is extracting and refactoring two already-validated contract families into reusable parameterizable templates plus a reference frontend and invisible-UX starter.

## 5. Maintenance Scope (3 months)

Applies only to the open-source template repo and examples delivered by this proposal — **NOT** to the proposer's existing 8 production contracts.

- Template issue triage, first response within 48 hours.
- Bug fixes for template code, build/test failures, broken examples.
- Dependency upgrades: CosmWasm, cw-plus, cw721-base, Rust, schema compatibility.
- Keep CI green and testnet examples deployable.
- Community PR initial review within 7 days.
- Update README and integration guide when code changes.
- Monthly public maintenance report.

Excluded: custom development, security audit, operation of existing production contracts, 24/7 support.

## 6. Trust Model & Non-Goals

The invisible-UX module discloses trust boundaries: who relays or pays gas, what users authorize, how session keys or custodial components work, and how users exit. This proposal does **NOT** claim "fully chainless" operation. It provides an optional UX pattern while contract settlement remains verifiable on-chain.

This proposal does **NOT** promise price appreciation, token rewards, mainnet lottery incentives, or broad user growth. The testnet lottery experience event uses testnet tokens only and is not gambling or investment.

## 7. Acceptance Criteria

- MIT repo public under Paxi Ecosystem org.
- Testnet contract addresses verifiable for both game and lottery contract families.
- React demo runs according to README.
- Invisible-UX demo completes at least one NFT mint and one PvP settlement without manual per-transaction signing, with documented trust boundaries.
- Docs cover build, deploy, integration, FAQ.
- Testnet lottery experience event targets at least 100 testnet interactions (target, not hard guarantee).
- Weekly public build log and monthly maintenance reports are public.

## 8. Timeline

- Week 1–2: repo setup, 三国 + choujiang code cleanup, parameterization, cw721-base traits.
- Week 3–4: testnet deploy, monitoring, React demo, invisible-UX example, lottery experience event.
- Week 5: docs, integration guide, FAQ.
- Month 2–4: maintenance, monthly reports.

## 9. Repo Plan

If the proposal passes, the repo will be created within 7 days under the Paxi Ecosystem org as `cosmwasm-game-template`, with an initial public README and issue tracker. Until then, no public URL is claimed to avoid misleading links.

## 10. Why

Paxi has 36 contracts running but lacks reusable open-source CosmWasm templates and a public invisible-UX integration pattern for games and lotteries. Existing activity is early: dozens of lottery interactions and 4 game contract upgrades. This proposal turns **two validated contract families** into public infrastructure, adds documentation and a testnet experience event, and lowers the barrier for new developers and players. The requested amount is about 3.05% of the DAO pool, with verifiable deliverables and scoped maintenance.
