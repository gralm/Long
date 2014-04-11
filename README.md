Long
====

Innehåller ett c++-bibliotek för högprecisionsvariabler.

class LongKalsong {

    int d;                  // d = exponenten. LongKalsong = sum: massaInts[i] * (2^16)^(d-i)
    int massaInts[massa];   // alla intsen, intsarna har 32 bitar, bara de 16 första används.
    bool sgn;               // beskriver om LongKalsongen är positiv eller negativ.

};

