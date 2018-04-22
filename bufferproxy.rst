==================
pygame.bufferproxy
==================


.. c:var:: PyTypeObject *pgBufproxy_Type

   The pygame buffer proxy object type pygame.BufferProxy.

.. c:function:: int pgBufproxy_Check(PyObject \*x)

   Return true if Python object x is a pgBufproxy_Type instance,
   false otherwise.
   This will return false on pgBufproxy_Type subclass instances as well.

.. c:function:: PyObject *pgBufproxy_New(PyObject \*obj, getbufferproc get_buffer)

   Return a new pygame.BufferProxy instance.
   Argument `obj` is the Python object that has its data exposed.
   Argument `get_buffer` is the :c:type::`pg_buffer` get callback.

.. c:function:: PyObject *pgBufproxy_GetParent(PyObject *obj)

   Return the Python object wrapped by buffer proxy `obj`.

.. c:function:: int pgBufproxy_Trip(PyObject *obj)

   Cause the buffer proxy object to create a 'pg_buffer' view of its parent.
   Return 0 on success, -1 otherwise.
