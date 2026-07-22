# Subnetwork Selection Results

This repository contains the node-level subnetwork selection results for 50 experiments. Each experiment contains three selected subnetworks.

## Files

- [`subnetwork_selection_results.xlsx`](subnetwork_selection_results.xlsx): original workbook, organized by experiment and subnetwork.
- [`subnetwork_selection_results.csv`](subnetwork_selection_results.csv): the same values in a flat, machine-readable table that GitHub can preview directly.

## Dataset summary

| Item | Count |
|---|---:|
| Experiments | 50 |
| Subnetworks | 150 |
| Node-level records | 552 |
| Anchor records | 150 |
| Member records | 402 |

The recorded eSINR values range from 6.08 to 11.64 dB, and the recorded KL-distance values range from 0.0000 to 2.8840.

## CSV columns

| Column | Description |
|---|---|
| `experiment_id` | Experiment identifier |
| `subnetwork_id` | Subnetwork identifier within the experiment |
| `role` | Node role: `Anchor` or `Member` |
| `node_id` | Node identifier |
| `source_id` | Source identifier |
| `esinr_db` | eSINR in decibels (dB) |
| `kl_distance` | KL-distance value recorded in the workbook |

Each CSV row represents one selected node. The experiment and subnetwork identifiers can be used together to reconstruct each selected subnetwork.

## Data preparation

The CSV was produced only by flattening the repeated `Exp_*` and `Subnet *` sections of the supplied workbook. Numeric measurements were not recalculated or otherwise transformed; eSINR is retained to two decimal places and KL distance to four decimal places.
