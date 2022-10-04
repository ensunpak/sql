/* MySQL code to query median value of a column */
/* lat_n is a column from station table in      */         
/* Hackerrank SQL challenge -                   */
/* Weather observation challenge 20             */

set @row_index := -1;

select round(avg(a.lat_n), 4) as median_latn
from
    (
    select
    @row_index := @row_index + 1 as row_index, lat_n
    from station
    order by lat_n) as a
where a.row_index
in (floor(@row_index / 2), ceil(@row_index / 2));
