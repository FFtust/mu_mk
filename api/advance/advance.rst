==================================
Advance
==================================

Some advance functions will be described here,  with this functions, you can control your halocode flexibly, it also means you need to be more careful.

:mod:`network2`
=============================================

Micropython has implemented a network module, see more in `network <http://docs.micropython.org/en/latest/library/network.html>`_.
the module network2 is based on network, and we add some other functions.

Default config::

  DEFAULT_AP_IP    = "192.168.4.1"
  DEFAULT_STA_IP   = "192.168.4.2"
  DEFAULT_NETMARK  = "255.255.255.0"
  DEFAULT_GATEWAY  = "192.168.1.1"
  DEFAULT_DNS      = "172.16.50.20"
  DEFAULT_AUTHMODE = AUTH_WPA2_PSK
  DEFAULT_PORT     = 5050

.. module:: network2
    :synopsis: network

**API REFERENCE**

.. function:: config_ap(ssid, password, authmode = DEFAULT_AUTHMODE, hidden = False)

    start as ap mode, ap+sta is not supported now.

.. function:: config_sta(ssid, password):  

    start as sta mode, ap+sta is not supported now.


.. function:: is_connected():


.. function:: set_ip(ip, if_mode = None):
  
  # set ip address


.. function:: set_subnet_mark(mark, if_mode = None):


.. function:: set_gateway(gw, if_mode = None):


.. function:: get_ip(if_mode = None):

.. function:: get_sunnet_mark(if_mode = None):

.. function:: get_gateway(if_mode = None):

.. function:: create_client():

.. function:: client_connect_to(ip_to, port = DEFAULT_PORT):

.. function:: create_server(port = DEFAULT_PORT):

.. function:: server_wait_connection(port = DEFAULT_PORT):

.. function:: server_get_connections(port = DEFAULT_PORT):


.. function:: server_get_latest_connection(port = DEFAULT_PORT):

.. function:: write(data, mode, ip_to, port = DEFAULT_PORT):


.. function:: write_line(data, mode, ip_to, port = DEFAULT_PORT):


.. function:: read(mode, ip_from, port = DEFAULT_PORT):


.. function:: read_line(mode, ip_from, port = DEFAULT_PORT):

example:
""""""""""""""""""""""""""""""""""

.. code-block:: python

  import halo
  halo.network2.config_sta("esp32_test", "12345678")


:mod:`communication`
=============================================

Halocode has implement a powerful communication mudle,  

.. function:: enable_channel_default(channel):


.. function:: disable_channel_default(channel):

.. function:: communication_o.disable_phy(channel_table[channel])

.. function:: enable_repl():

.. function:: disable_repl():

.. function:: read(channel):


.. function:: send(channel):

.. function:: bind_passthrough_channels(channel1, channel2):

.. function:: unbind_passthrough_channels(channel1, channel2):


:mod:`game`
=============================================

`System functions`
=============================================
::
    halo.print_user_script()

