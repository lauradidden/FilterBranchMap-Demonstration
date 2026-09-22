# Local lightweight LogView

This local `logview` package is a self-contained compatibility layer for FilterBranchMap. It keeps the original LogView-style imports and query syntax while delegating filtering to PM4Py.

Supported original predicates:

- `EqToConstant`
- `NotEqToConstant`
- `GreaterThanConstant`
- `GreaterEqualToConstant`
- `LessThanConstant`
- `LessEqualToConstant`
- `StartWith`
- `EndWith`
- `DurationWithin`
- `Union`
- `Query`

Additional PM4Py case-preserving predicates:

- `EventAttributeValues`
- `TraceAttributeValues`
- `Variants`
- `DirectlyFollowsRelation`
- `EventuallyFollowsRelation`
- `TimeRange` with `mode='traces_contained'` or `mode='traces_intersecting'`
- `CaseSize`
- `CasePerformance`
- `ActivitiesRework`
- `PathsPerformance`

Unsupported by design:

- OCEL filters
- `filter_between`
- `filter_prefixes`
- `filter_suffixes`
- event-level filters that remove individual events from cases
- `filter_time_range(..., mode='events')`

Example:

```python
from logview.utils import LogViewBuilder
from logview.predicate import *

log_view = LogViewBuilder.build_log_view(log)

query = Query('TopVariants', [VariantsTopK(5)])
result_set, complement = log_view.evaluate_query('rs_TopVariants', log, query)

summary = log_view.get_summary()
```
