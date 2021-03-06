storm-integration  --- EXPERIMENTAL ---
=================

##XAP/Storm integration

This repo contains projects related to the effort to integrate Storm and XAP in various ways.  Cloudify is used as a means of packaging the various projects in the form of recipes.  Currently the recipes are targeted at AWS only.  As such, the repo is divided into two folders: _Cloudify_ and _XAP_.  Cloudify recipes are contained in the _Cloudify_ folder, and source code used to create system components (e.g. plugins, streaming support) are placed in the _XAP_ folder.

#####Recipes
* xap9.1-lite service
  Single node XAP 9.1 Lite recipe.  Uses XAP default for the most part.
* xapstream service
  Recipe subclass of xap9.1-lite. Just deploys streaming pu into XAP.
* streamdriver service
  Utility recipe that creates/connects to streams and writes tuples for testing.

####XAP Components
* storm
  Storm specific java code.  The XAP Spout and Trident State implementation are here.
* streamspace-pu
  The processing unit deployed by xapstream.  XAP resident code that support streaming.
* storm-test-topology
  Home of topologies for testing the XAP+Storm infrastructure (e.g. WordCount).
* streaming
  Storm independent tuple streaming code that the XAP Spout depends upon.
