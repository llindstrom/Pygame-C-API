==============
pygame.display
==============


.. c:type:: pgVidInfoObject

   A pygame object that wraps an SDL_VideoInfo struct.

.. c:var:: PyTypeObject *pgVidInfo_Type

   The Python type of a pgVidInfoObject instance.

.. c:function:: SDL_VideoInfo pgVidInfo_AsVidInfo(PyObject *obj)

   A macro to access the SDL_VideoInfo field of a pgVidInfo_Type instance.

.. c:function:: PyObject *pgVidInfo_New(SDL_VideoInfo *i)

   Return a new pgVidInfo_Type instance from the SDL_VideoInfo `i`.
   On failure, raise a Python exception and return NULL.

.. c:function:: int pgSurface_Check(PyObject *x)

   Return true if `x` is a pgVidInfo_Type instance

   Will return false if `x` is a subclass of Surface.
   This is a macro. No check is made that `x` is not NULL.
