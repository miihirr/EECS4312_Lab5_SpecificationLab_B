# Constraints and Assumptions for is_allocation_feasible()

## Constraints

**C1:** All requests must be dictionaries; non-dict requests raise `ValueError`.

**C2:** All requested resources must exist in available resources; missing resources return False.

**C3:** Total demand for any resource cannot exceed its available capacity.

**C4:** Resource capacities and request amounts must be numeric (int or float).

---

## Assumptions

**A1:** All resource capacities and request amounts are non-negative.

**A2:** Resources are independent; allocation of one doesn't affect another.

**A3:** If total demand ≤ capacity for all resources, allocation is feasible (greedy strategy).

**A4:** Input data is well-formed and consistent from trusted sources.

**A5:** Resource requests are all-or-nothing; no partial fulfillment allowed.

**A6:** Each function call is independent with no state maintained between calls.
