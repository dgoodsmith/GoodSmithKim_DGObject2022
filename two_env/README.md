Data for remapping experiments in two distinct environments (Figures 7 and S5)


Contains:

* two_env_maps: speed filtered rate maps for all 57 active cells. Each row is one cell, and the five columns contain the five recording sessions (STD-A, MAN-A, STD-B, MAN-B, STD-A')
* two_env_class: classification of the 57 active cells, 1 = granule cell, 0 = mossy cell
* two_env_active: value of 1 indicates a statstically significant place field was detected in the session
* two_env_std_correlations: correlations between STD sessions in A and A' (stda_stda_gc, stda_stda_mc) and between STD sessions in A and B (stda_stdb_gc, stda_stdb_mc)
* two_env_std_correations_rotate: correlations between STD sessions after rotating rate maps in 90 degree increments. All four rotation values are given (\*_rot_mc and \*_rot_gc files) as well as the maximum valuses (/*_max files)
* two_env_object: object locations for each session, each row is one object and columns represent x and y coordinates in rate map pixels
* two_env_assignments: the subjective response types assigned by each of three observers. 95 Pairs of std and MAN sessions were presented in random order. contains:
  1) cellno: for each of the 95 session pairs, the cell number (1-57 corresponding to rate maps). The first 50 are sessions 1/2 (ENVA) and the next 45 are sessions 3/4 (ENVB).
  2) obs1, obs2, obs3: subjective assessments of each of three observers. For each observer, the first three columns are the assessments provided through three independent and random passes of all session pairs. The fourth column for each observer is the response selected at least 2/3 times (NaN indicates no response selected twice). Possible responses were: 0 - no object response, 1 - moved field, 2 - field appeared, 3 - field disappeared, 4 - trace, 5 - capture, NaN - ambiguous. Multiple responses could be selected, for example 12 would indicate one field moved and antoher appeared.
  3) consensus: for each of the 95 session pairs, the response selected by at least 2/3 observers. NaN indicates no response was selected by at least two observers.
