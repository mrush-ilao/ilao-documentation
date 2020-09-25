==============================
Guided Navigation API Docs
==============================

Stored variables
==================
ILAO stores in Drupal configuration:

* API Server location (https://[sitename].legalserver.org/api/v1/processes for example)
* Username authorized to use API
* Password associated with the username

API Invocations
===================

Get list of processes
------------------------
This code snippet returns the list of processes available to Guided navigation


.. code-block:: php

    $gn = ilao_gn_load_keys();
    $url = $gn['server'];
    $ch = curl_init();
    curl_setopt($ch, CURLOPT_URL, $url);
    curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
    curl_setopt($ch, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
    curl_setopt($ch, CURLOPT_USERPWD, $gn['user'] . ':' . $gn['pass']);
    $result = curl_exec($ch);
    $processes = json_decode($result);
    return $processes;
    
Start a new session for a specific Guided Navigation process
---------------------------------------------------------------

.. code-block:: php

    $gn = ilao_gn_load_keys();
    $url = $gn['server'] . '/' . $intake_id . '/sessions';
    $ch = curl_init();
    curl_setopt($ch, CURLOPT_URL, $url);
    curl_setopt($ch, CURLOPT_CONNECTTIMEOUT, 20);
    curl_setopt($ch, CURLOPT_CUSTOMREQUEST, "POST");
    curl_setopt($ch, CURLOPT_POST, true);
    //  curl_setopt($ch, CURLOPT_POSTFIELDS, $data_string);
    curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
    curl_setopt($ch, CURLOPT_USERPWD, $gn['user'] . ':' . $gn['pass']);
    curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, false);
    curl_setopt($ch, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
    curl_setopt($ch, CURLOPT_HTTPHEADER, array(
            'Accept: application/json',
            'Content-Type: application/json')
    );
    $result = curl_exec($ch);
    $start = json_decode($result);
    return $start;

.. note:: in the above example, $intake_id represents the process ID from the list of processes.   
    