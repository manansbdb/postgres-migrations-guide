# Best Practices / Boas Práticas

## English
- One logical change per migration; keep them idempotent when possible.
- Prefer `ADD COLUMN ... NULL` then backfill, then constrain.
- Create indexes concurrently on large tables (`CREATE INDEX CONCURRENTLY`).
- Never rename/drop columns in the same deploy that still reads the old shape.
- Backup / take a snapshot before risky production migrations.
- Test up and down (or expand/contract) paths in CI against a real Postgres.

## Português
- Uma mudança lógica por migration; mantenha-as idempotentes quando possível.
- Prefira `ADD COLUMN ... NULL`, depois backfill, depois constraint.
- Crie indexes concurrentemente em tabelas grandes (`CREATE INDEX CONCURRENTLY`).
- Não renomeie/remova colunas no mesmo deploy que ainda lê o formato antigo.
- Faça backup/snapshot antes de migrations arriscadas em produção.
- Teste caminhos up/down (ou expand/contract) no CI contra Postgres real.
