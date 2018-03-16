    AP#:      7
    Repo:     pinus-rigida
    Title:    Agathis Trunk Hardware Specifications
    Author:   md-agathisproject
	License:  CC-BY-SA 4.0

# Agathis Trunk Hardware Specifications

## Table of Content

[1. Introduction](#1-introduction)  
[2. Terminology](#2-terminology)  
[3. Tree Architecture](#3-tree-architecture)  
[4. Trunk Mechanical Specifications](#4-trunk-mechanical-specifications)  
[5. Trunk Electrical Specifications](#5-trunk-electrical-specifications)  

## 1. Introduction

* This document describes the electrical and mechanical specifications
for the trunk interface of the Agathis gateway and provides simple and
precise details needed to understand its operation or develop new
modules or variants.

* Audience: modules and systems implementers.

* Agathis Trunk is the core of the Agathis Project, supporting all
the other parts of the system for optimal functionality,
interoperability and evolution.

## 2. Terminology

This specification uses special CAPITALIZED keywords:

RULE: a rule SHALL be followed to ensure compatibility. A rule is
triggered by the words SHALL and SHALL NOT.

RECOMMENDATION: a recommendation affects the usability of the
implementation. A recommendation is triggered by the words SHOULD and
SHOULD NOT.

PERMISSION: a permission clarifies the details that are not specifically
prohibited. A permission is triggered by the word MAY.

SHALL: indicates a mandatory requirement - it triggers a RULE.

SHOULD: indicates flexibility of choice with a strongly preferred
implementation - it triggers a RECOMMENDATION.

MAY: indicates flexibility of choice with no implied preference - it
triggers a PERMISSION.

**Tree:** is a stack of one power module, one or more root modules and
one or more branch modules.

**Power module:** adapts and stores external energy; it may include
Ethernet PoE functions. There is one and only one power module in a tree
and it always occupies the first position in the stack.

**Root:** is a module that controls the modules stacked above, up to
another root; there is at least one root in a tree, stacked on top
of the power module; the root is the brain of the tree; if more brain
power is needed, then multiple roots can be stacked together. A root
behaves as a branch for the root below.

**Branch:** is a module stacked above a root or another branch; its main
functions are to connect the tree to the external world or to provide
internal features to the gateway.

**Trunk:** connects the power, root and branch modules to form a an
integrated power distribution and communication system.

## 3. Tree Architecture

+++ one or more diagrams to identify the modules, the cages, the trunk connectors, power rails and signal interfaces - NOTHING MORE THAN THIS

+++ explanation to said diagram

## 4. Trunk Mechanical Specifications

## 5. Trunk Electrical Specifications
[5.1. Power Distribution](#51-power-distribution)

### 5.1. Power Distribution


### 5.2. Signal Interface



