# Contribution and Update Flow

## Recommended flow
1. import or update a source asset
2. adjust adapters
3. update validation docs if behavior expectations changed
4. run at least one validation pass
5. update result docs
6. update the wiki if usage or structure changed

## Branch strategy
- `main` is the stable default branch
- use `import/<name>` for new source imports
- use `validate/<name>` for focused validation rounds
- use `docs/<name>` for documentation-only refinement when helpful

Recommended pattern:
1. branch from `main`
2. make the import / validation / docs change
3. commit with lore-style context
4. push branch
5. optionally open an internal PR back to `main`

## Global requirement
This repo follows the wiki lifecycle policy:
- create wiki at start
- update it at finish
- revise it at least once after first creation
