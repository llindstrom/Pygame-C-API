============
pygame.event
============

.. c:type:: pgEventObject

   A pygame event instance.

   .. c:member:: int type

      The event type code.

.. c:var:: pgEvent_Type

   The pygame event object type pygame.event.EventType.

.. c:function:: int pgEvent_Check(PyObject *x)

   Return true if `x` is a pygame event instance

   Will return false if `x` is a subclass of event.
   This is a macro. No check is made that `x` is not NULL.

.. c:function:: PyObject *pgEvent_New(SDL_Event *event)

   Return a new pygame event instance for SDL `event`.
   Return NULL on error.

.. c:function:: PyObject *pgEvent_New2(int type, PyObject *dict)

   Return a new pygame event instance of SDL `type` and with
   attribute dictionary `dict`.
   If `dict` is NULL and empty attribute dictionary is created.
   Return NULL on error.

.. c:function:: int pgEvent_FillUserEvent(pgEventObject *e, SDL_Event *event)

   Fill SDL event `event` with information from pygame user event instance `e`.
   Return 0 on success, -1 otherwise.
