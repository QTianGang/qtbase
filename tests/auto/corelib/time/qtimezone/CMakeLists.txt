# Generated from qtimezone.pro.

#####################################################################
## tst_qtimezone Test:
#####################################################################

qt_add_test(tst_qtimezone
    SOURCES
        tst_qtimezone.cpp
    DEFINES
        QT_NO_FOREACH
        QT_NO_KEYWORDS
    PUBLIC_LIBRARIES
        Qt::CorePrivate
)

## Scopes:
#####################################################################

qt_extend_target(tst_qtimezone CONDITION QT_FEATURE_icu
    LIBRARIES
        ICU::i18n ICU::uc ICU::data
)

qt_extend_target(tst_qtimezone CONDITION APPLE
    SOURCES
        tst_qtimezone_darwin.mm
    PUBLIC_LIBRARIES
        ${FWFoundation}
)
