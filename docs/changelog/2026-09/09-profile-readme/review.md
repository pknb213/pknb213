# Independent profile claims review

Reviewed 2026-09-09 against sibling `pknb213.github.io/src/data/portfolio.ts` and `src/data/openSourceProjects.ts`.

## Result

No quantitative mismatches or misleading work/learning claims found. The parent resolved the two initial technology attribution gaps against the corresponding dependency files. No blocking findings remain.

## Findings

- README line 28: `FastAPI` is assigned to cms-rag, but the named portfolio sources explicitly identify FastAPI only for cms-api. This is missing evidence, not evidence that the label is false.
- README line 36: `SQLAlchemy` is assigned to cms-api, but the named sources identify SQLAlchemy only under Python-Projects. Confirm its cms-api dependency before publication.

## Verified

- cms-rag: 23,601 source/index records, two vector adapters, 58 test functions; rebuild/swap and incremental-event descriptions match `repositoryProfiles['cms-rag']` and `evidenceLedger`.
- cms-api: 14 API routes, nine Alembic migrations, 19 test functions; job persistence, worker state ownership, and separate index events match `repositoryProfiles['cms-api']`.
- July 2026 snapshot language and development-environment limitation match the source snapshots. README correctly avoids claiming pass rate, coverage, production traffic, or production search-quality improvement.
- Python-Projects, Kotlin-SpringBoot-Servers, TypeScript-Servers, and LangChain-Challenge names match the public-project inventory. Their feature summaries and table technologies match the implementation descriptions, including TypeScript Redis through its socket.io Redis adapter.
- LangChain course attribution and the distinction between personal learning repositories and professional case studies are explicit and consistent with source descriptions.
- All portfolio hash targets used by README appear in the `RouteId` union.
- The broader data-platform statement is corroborated by supplemental literal checks in `src/data/dataPlatforms.ts` (stream/storage) and `src/data/careerProjects.ts` (collection and observability).

## Limits

This is a source-consistency review, not independent execution of private systems, a recount of test functions, or a live GitHub visibility/link check. The parent task owns live link/render verification. No project code was changed.

## Parent resolution

- cms-rag/pyproject.toml line 10 declares FastAPI.
- cms-api/pyproject.toml line 16 declares SQLAlchemy.
- The public repository table was subsequently changed to a stacked list for mobile readability; claims and technology labels are unchanged.
