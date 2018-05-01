============
pygame.mixer
============


.. c:type:: pgSoundObject

   The pygame.mixer.Sound instance C structure.

.. c:var:: PyTypeObject *pgSound_Type

   The pygame.mixer.Sound Python type.

.. c:function:: PyObject \*pgSound_New(Mix_Chunk \*chunk)

   Return a new pygame.mixer.Sound instance for the SDL mixer chunk 'chunk'.
   On failure, raise a Python exception and return NULL.

.. c:function:: int pgSound_Check(PyObject \*obj)

   Return true if `obj` is an instance of type c:var::`pgSound_Type`,
   but not a c:var::`pgSound_Type` subclass instance.
   A macro.

.. c:function:: Mix_Chunk \*pgSound_AsChunk(PyObject \*x)

   Return the SDL Mix_Chunk struct associated with the pgSound_Type
   instance `x`.
   A macro that does no NULL or Python type check on `x`.

.. c:type:: pgChannelObject

   The pygame.mixer.Channel instance C structure.

.. c:var:: PyTypeObject \*pgChannel_Type

   The pygame.mixer.Channel Python type.

.. c:function:: PyObject \*pgChannel_New(int channelnum)

   Return a new pygame.mixer.Channel instance for the SDL mixer channel `channelnum`.
   On failure, raise a Python exception and return NULL.

.. c:function:: int pgChannel_Check(PyObject \*obj)

   Return true if `obj` is an instance of type c:var::`pgChannel_Type`,
   but not a c:var::`pgChannel_Type` subclass instance.
   A macro.

.. c:function:: Mix_Chunk \*pgChannel_AsInt(PyObject \*x)

   Return the SDL mixer music channel number associated with c:var::`pgChannel_Type` instance `x`.
   A macro that does no NULL or Python type check on `x`.

.. c:function:: void pgMixer_AutoInit(void)

   Initializes the pygame.mixer module and start the SDL mixer

.. c:function:: void pgMixer_AutoQuit(void)

   Stop all playing channels and close the SDL mixer
