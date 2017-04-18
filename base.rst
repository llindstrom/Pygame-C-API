===========
pygame.base
===========


.. c:var:: PyObject *pgExc_SDLError

   This is pygame.error, the exception type used to raise SDL errors.

.. c:function:: int pgVideo_AutoInit()

.. c:function:: void pgVideo_AutoQuit()

.. c:function:: void pg_RegisterQuit(void (*f)(void))

   Register function *f* as a callback on Pygame termination.
   Multiple functions can be registered.
   Functions are called in the order they were registered.

.. c:function:: int pg_IntFromObj(PyObject *o, int *v)

   Convert number like object *o* to C int and place in argument *v*.
   Return 1 on success, else 0.
   No Python exceptions are raised.

.. c:function:: int pg_IntFromObjIndex(PyObject *o, int i, int *v)

   Convert number like object at position *i* in sequence *o*
   to C int and place in argument *v*.
   Return 1 on success, else raise a Python exception and return 0.

.. c:function:: int pg_TwoIntsFromObj(PyObject *o, int *v1, int *v2)

   Convert the two number like objects in length 2 sequence *o*
   to C int and place in arguments *v1* and *v2* respectively.
   Return 1 on success, else raise a Python exception and return 0.

.. c:function:: int pg_FloatFromObj(PyObject *o, float *v)

   Convert number like object *o* to C float and place in argument *v*.
   Returns 1 on success, 0 on failure.
   No Python exceptions are raised.


.. c:function:: int pg_FloatFromObjIndex(PyObject *o, int i, float *v)

   Convert number like object at position *i* in sequence *o*
   to C float and place in argument *v*.
   Return 1 on success, else raise a Python exception and return 0.

.. c:function:: int pg_TwoFloatsFromObj(PyObject *o, float *v1, float *v2)

   Convert the two number like objects in length 2 sequence *o*
   to C float and place in arguments *v1* and *v2* respectively.
   Return 1 on success, else raise a Python exception and return 0.

.. c:function:: int pg_UintFromObj(PyObject *o, Uint32 *v)

   Convert number like object *o* to unsigned 32 bit integer and place
   in argument *v*.
   Return 1 on success, else 0.
   No Python exceptions are raised.

.. c:function:: int pg_UintFromObjIndex(PyObject *obj, int _index, Uint32 *val)

   Convert number like object at position *i* in sequence *o*
   to unsigned 32 bit integer and place in argument *v*.
   Return 1 on success, else raise a Python exception and return 0.

.. c:function:: int pg_RGBAFromObj(PyObject *o, Uint8 *c)

.. c:type:: pybuffer_releaseproc

   A pointer to a buffer destructor function of signature void f(Py_buffer \*).

.. c:type:: pg_buffer

   .. c:member:: Py_buffer view

   .. c:member:: PyObject* consumer

   .. c:member:: pybuffer_releaseproc release_buffer

.. c:var:: PyObject *pgExc_BufferError

.. c:function:: PyObject *pgBuffer_AsArrayInterface(Py_buffer *b)

.. c:function:: PyObject *pgBuffer_AsArrayStruct(Py_buffer *b)

.. c:function:: int pgObject_GetBuffer(PyObject *o, Pg_buffer *b, int flags)

.. c:function:: void pgBuffer_Release(Pg_buffer *b)

.. c:function:: int pgDict_AsBuffer(Pg_buffer *b, PyObject *o, int flags)

.. c:function:: void import_pygame_base()

