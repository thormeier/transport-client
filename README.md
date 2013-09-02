ThormeierTransportClientBundle
==============================

[![Build Status](https://travis-ci.org/thormeier/transport-client-bundle.png?branch=master)](https://travis-ci.org/thormeier/transport-client)

## Introduction

This bundle provides simple access to the [OpenData Transport API](http://transport.opendata.ch/) in Symfony2. The Transport API provides Swiss public transport data, that is converted into instances of Doctrine-like entity classes within this bundle for further usage.

    <?php
    
    $transportClient = $this->container->get('transport.client');

This bundle provides a new `transport.client` service that returns an instance of `Thormeier\TransportClientBundle\Service\Transport`

## Installation

### Step 1: Composer require

    $ php composer.phar require "thormeier/transport-bundle":"1.0.1"

### Step2: Enable the bundle in the kernel


    <?php
    // app/AppKernel.php

    public function registerBundles()
    {
        $bundles = array(
            // ...
            new Thormeier\TransportClientBundle\ThormeierTransportClientBundle(),
            // ...
        );
    }