===========
pygame.base
===========

.. c:type:: Pg_buffer

.. c:var:: PyObject *PyExc_SDLError

.. c:function:: void PyGame_RegisterQuit()

.. c:function:: int IntFromObj(PyObject *o, int *v)

.. c:function:: int IntFromObjIndex(PyObject *o, int i, int *v)

.. c:function:: int TwoIntsFromObj(PyObject *o, int *v1, int *v2)

.. c:function:: int FloatFromObj(PyObject *o, float *v)

.. c:function:: int FloatFromObjIndex(PyObject *o, int i, float *v)

.. c:function:: int TwoFloatsFromObj(PyObject *o, float *v1, float *v2)

.. c:function:: int UIntFromObj(PyObject *o, Uint32 *v)

.. c:function:: int UIntFromObjIndex(PyObject *o, int i, Uint32 *v)

.. c:function:: void PyGame_Video_AutoQuit()

.. c:function:: int PyGame_Video_AutoInit()

.. c:function:: int RGBAFromObj(PyObject *o, Uint8 *c)

.. c:function:: PyObject *PgBuffer_AsArrayInterface(Py_buffer *b)

.. c:function:: PyObject *PgBuffer_AsArrayStruct(Py_buffer *b)

.. c:function:: int PgObject_GetBuffer(PyObject *o, Pg_buffer *b, int flags)

.. c:function:: void PgBuffer_Release(Pg_buffer *b)

.. c:function:: int PgDict_AsBuffer(Pg_buffer *b, PyObject *o, int flags)

.. c:var:: PyObject *PgExc_BufferError

.. c:function:: void import_pygame_base()

