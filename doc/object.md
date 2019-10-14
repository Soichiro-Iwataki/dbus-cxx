
  
  @example calculator_server.cpp
 
  This example is one part of three example applications that demonstrate
  client, server and watcher applications that use adapters and proxies
  generated by dbus-cxx-xml2cpp from a modified dbus introspection XML
  document.
 
  These three examples are:
  
  * \c calculator_server.cpp
  * \c calculator_client.cpp
  * \c calculator_watcher.cpp
  
 
  This particular piece is the server that uses the generated Object
  derived class to provide an adapter interface for the Calculator
  class.
 
  Here is the calculator class, which by itself knows nothing of dbus:
 
  @include xml2cpp/calculator/calculator.h
  @include xml2cpp/calculator/calculator.cpp
 
  The adapter is generated with this command:
  @code
  dbus-cxx-xml2cpp --xml calculator.xml --adapter -f
  @endcode
 
  The modified introspection XML document is here:
  @include xml2cpp/calculator/calculator.xml
 
  Here is the generated adapter:
  @include xml2cpp/calculator/calculator_adapter.h
 
  And here is the server application:
 


  
  @defgroup local Local Objects
 
  This group contains objects which are natively local and
  provide interfaces such as methods and signals that can
  be exported to dbus.


  
  @defgroup objects Objects
