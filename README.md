# GitOps Architecture Examples (Kargo + Kro + Argo CD)

**Single source of truth:** Git. **Change unit:** image tag (SemVer).
**Responsibilities:** Kargo decides/promotes/rolls back → Git commit → Argo CD reconciles → Kro renders resources.

## Quick Navigation

* Argo CD ApplicationSet: `argocd/applicationsets/develop-applicationset.yaml`
* Kro Instance (frontend-dev): `kro/instances/instance.yaml`
* Kargo

  * Warehouse: `kargo/warehouses/frontend-dev-image.yaml`
  * Stage: `kargo/stages/frontend-dev-stage.yaml`
  * PromotionTask: `kargo/tasks/promote-kro-instance.yaml`

## Related Medium Articles

1. Why Argo CD Wasn’t Enough — Real GitOps Pain and the Tools That Fixed It
2. How Kro RGD Helped Me Clean Up and Trace My GitOps Deployments
3. Designing a Maintainable GitOps Repo Structure — Managing Multi-Service & Multi-Env with Argo CD
4. GitOps Promotion with Kargo — Image Tag → Git Commit → Argo Sync
5. Implementing a Modular Kargo Promotion Workflow — Extracting PromotionTask from Stage for Long-Term Maintainability
6. Designing a Maintainable GitOps Architecture — How I Scaled My Promotion Flow

> Each article maps to example YAML files listed in `examples-index.md`.
