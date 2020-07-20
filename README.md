# OpenShift API for Rust

[![CI](https://github.com/ctron/openshift-openapi/workflows/CI/badge.svg)](https://github.com/ctron/openshift-openapi/actions?query=workflow%3ACI)
[![Crates.io version shield](https://img.shields.io/crates/v/openshift-openapi.svg)](https://crates.io/crates/openshift-openapi)
[![Docs](https://docs.rs/openshift-openapi/badge.svg)](https://docs.rs/openshift-openapi)
[![Crates.io license shield](https://img.shields.io/crates/l/openshift-openapi.svg)](https://crates.io/crates/openshift-openapi)

This crate is a Rust OpenShift API client. It contains bindings for the
resources and operations in the OpenShift client API,
auto-generated from the OpenAPI spec.

## Builds on `k8s_openapi`

This work is based on the wonderful work from https://github.com/Arnavion/k8s-openapi. It does not contain
the Kubernetes APIs, that is handled by the `k8s_openapi` crate. It only contains the types added by OpenShift
(like `Route` and `ImageStream`) and references the existing Kubernetes (like `Pod` and `Deployment`) from the
`k8s_openapi` crate.

## OpenShift Versions

| OpenShift Version | Feature | Kubernetes Version | `k8s_openapi` Feature |
| ----------------- | ------- | ------------------ | --------------------- |
| 4.2.x             | `v4_2`  | 1.15.x             | `v1_15`               |
| 4.3.x             | `v4_3`  | 1.16.x             | `v1_16`               |
| 4.4.x             | `v4_4`  | 1.17.x             | `v1_17`               |
| 4.5.x             | `v4_5`  | 1.18.x             | `v1_18`               |

**Note:** Enabling a version feature (for example`v4_4`) in this crate, will automatically
enable the corresponding feature (`v1_17`) for the `k8s_openapi` crate.
