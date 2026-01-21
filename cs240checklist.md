Passoff Tests (22 passed, 42 failed)
    piecemoves (6 passed, 42 failed)
        KingMoveTests (1 passed, 2 failed)
            kingBlocked() ✓
            kingCaptureEnemy() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=3, column=4}, end=ChessPosition{row=2, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=4}, end=ChessPosition{row=3, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=4}, end=ChessPosition{row=3, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=4}, end=ChessPosition{row=4, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=4}, end=ChessPosition{row=4, column=4}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KingMoveTests.kingCaptureEnemy(KingMoveTests.java:29)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            kingMiddleOfBoard() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=3, column=6}, end=ChessPosition{row=2, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=6}, end=ChessPosition{row=2, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=6}, end=ChessPosition{row=2, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=6}, end=ChessPosition{row=3, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=6}, end=ChessPosition{row=3, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=6}, end=ChessPosition{row=4, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=6}, end=ChessPosition{row=4, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=6}, end=ChessPosition{row=4, column=7}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KingMoveTests.kingMiddleOfBoard(KingMoveTests.java:11)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

        PawnMoveTests (2 passed, 21 failed)
            pawnCaptureBlack() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=4, column=4}, end=ChessPosition{row=3, column=5}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnCaptureBlack(PawnMoveTests.java:227)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnCaptureWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=4, column=4}, end=ChessPosition{row=5, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=4}, end=ChessPosition{row=5, column=4}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=4, column=4}, end=ChessPosition{row=5, column=4}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnCaptureWhite(PawnMoveTests.java:210)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            edgePromotionBlack() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=1, column=3}, promotion=QUEEN}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=1, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=1, column=3}, promotion=KNIGHT}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=1, column=3}, promotion=ROOK}]> but was: <[ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=1, column=3}, promotion=QUEEN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.piecemoves.PawnMoveTests.validatePromotion(PawnMoveTests.java:426)
at passoff.chess.piecemoves.PawnMoveTests.edgePromotionBlack(PawnMoveTests.java:104)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnPromotionWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=7, column=3}, end=ChessPosition{row=8, column=3}, promotion=QUEEN}, ChessMove{start=ChessPosition{row=7, column=3}, end=ChessPosition{row=8, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=3}, end=ChessPosition{row=8, column=3}, promotion=KNIGHT}, ChessMove{start=ChessPosition{row=7, column=3}, end=ChessPosition{row=8, column=3}, promotion=ROOK}]> but was: <[ChessMove{start=ChessPosition{row=7, column=3}, end=ChessPosition{row=8, column=3}, promotion=QUEEN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.piecemoves.PawnMoveTests.validatePromotion(PawnMoveTests.java:426)
at passoff.chess.piecemoves.PawnMoveTests.pawnPromotionWhite(PawnMoveTests.java:86)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnInitialMoveBlack() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=7, column=3}, end=ChessPosition{row=5, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=3}, end=ChessPosition{row=6, column=3}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=7, column=3}, end=ChessPosition{row=6, column=3}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnInitialMoveBlack(PawnMoveTests.java:68)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnInitialMoveWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=2, column=5}, end=ChessPosition{row=3, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=5}, end=ChessPosition{row=4, column=5}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=2, column=5}, end=ChessPosition{row=3, column=5}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnInitialMoveWhite(PawnMoveTests.java:51)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnPromotionCapture() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=2, column=2}, end=ChessPosition{row=1, column=1}, promotion=QUEEN}, ChessMove{start=ChessPosition{row=2, column=2}, end=ChessPosition{row=1, column=1}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=2}, end=ChessPosition{row=1, column=1}, promotion=KNIGHT}, ChessMove{start=ChessPosition{row=2, column=2}, end=ChessPosition{row=1, column=1}, promotion=ROOK}, ChessMove{start=ChessPosition{row=2, column=2}, end=ChessPosition{row=1, column=2}, promotion=QUEEN}, ChessMove{start=ChessPosition{row=2, column=2}, end=ChessPosition{row=1, column=2}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=2}, end=ChessPosition{row=1, column=2}, promotion=KNIGHT}, ChessMove{start=ChessPosition{row=2, column=2}, end=ChessPosition{row=1, column=2}, promotion=ROOK}]> but was: <[ChessMove{start=ChessPosition{row=2, column=2}, end=ChessPosition{row=1, column=2}, promotion=QUEEN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.piecemoves.PawnMoveTests.validatePromotion(PawnMoveTests.java:426)
at passoff.chess.piecemoves.PawnMoveTests.pawnPromotionCapture(PawnMoveTests.java:122)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnMoveFromEdgeBlack() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=5, column=8}, end=ChessPosition{row=4, column=8}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=5, column=8}, end=ChessPosition{row=4, column=8}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnMoveFromEdgeBlack(PawnMoveTests.java:261)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnMoveFromEdgeWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=4, column=8}, end=ChessPosition{row=5, column=8}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=4, column=8}, end=ChessPosition{row=5, column=8}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnMoveFromEdgeWhite(PawnMoveTests.java:244)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            captureAndPromoteBlack() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=1, column=3}, promotion=QUEEN}, ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=1, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=1, column=3}, promotion=KNIGHT}, ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=1, column=3}, promotion=ROOK}, ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=1, column=4}, promotion=QUEEN}, ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=1, column=4}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=1, column=4}, promotion=KNIGHT}, ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=1, column=4}, promotion=ROOK}]> but was: <[ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=1, column=4}, promotion=QUEEN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.piecemoves.PawnMoveTests.validatePromotion(PawnMoveTests.java:426)
at passoff.chess.piecemoves.PawnMoveTests.captureAndPromoteBlack(PawnMoveTests.java:363)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            captureAndPromoteWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=8, column=3}, promotion=QUEEN}, ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=8, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=8, column=3}, promotion=KNIGHT}, ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=8, column=3}, promotion=ROOK}, ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=8, column=4}, promotion=QUEEN}, ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=8, column=4}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=8, column=4}, promotion=KNIGHT}, ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=8, column=4}, promotion=ROOK}]> but was: <[ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=8, column=4}, promotion=QUEEN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.piecemoves.PawnMoveTests.validatePromotion(PawnMoveTests.java:426)
at passoff.chess.piecemoves.PawnMoveTests.captureAndPromoteWhite(PawnMoveTests.java:346)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnAdvanceBlockedWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[]> but was: <[ChessMove{start=ChessPosition{row=4, column=4}, end=ChessPosition{row=5, column=3}, promotion=PAWN}, ChessMove{start=ChessPosition{row=4, column=4}, end=ChessPosition{row=5, column=5}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnAdvanceBlockedWhite(PawnMoveTests.java:140)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnMiddleOfBoardBlack() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=4, column=4}, end=ChessPosition{row=3, column=4}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=4, column=4}, end=ChessPosition{row=3, column=4}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnMiddleOfBoardBlack(PawnMoveTests.java:33)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnMiddleOfBoardWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=4, column=4}, end=ChessPosition{row=5, column=4}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=4, column=4}, end=ChessPosition{row=5, column=4}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnMiddleOfBoardWhite(PawnMoveTests.java:16)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnAdvanceBlockedBlack() ✓
            pawnCaptureFromEdgeBlack() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=5, column=8}, end=ChessPosition{row=4, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=8}, end=ChessPosition{row=4, column=8}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=5, column=8}, end=ChessPosition{row=4, column=8}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnCaptureFromEdgeBlack(PawnMoveTests.java:295)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnCaptureFromEdgeWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=4, column=8}, end=ChessPosition{row=5, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=8}, end=ChessPosition{row=5, column=8}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=4, column=8}, end=ChessPosition{row=5, column=8}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnCaptureFromEdgeWhite(PawnMoveTests.java:278)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnCaptureFromStartBlack() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=5, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=6, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=6, column=4}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=7, column=4}, end=ChessPosition{row=6, column=4}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnCaptureFromStartBlack(PawnMoveTests.java:329)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnCaptureFromStartWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=3, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=3, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=4, column=4}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=2, column=4}, end=ChessPosition{row=3, column=4}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnCaptureFromStartWhite(PawnMoveTests.java:312)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnCannotCaptureBackwardBlack() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=6, column=3}, end=ChessPosition{row=5, column=3}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=6, column=3}, end=ChessPosition{row=5, column=3}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnCannotCaptureBackwardBlack(PawnMoveTests.java:397)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnCannotCaptureBackwardWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=3, column=3}, end=ChessPosition{row=4, column=3}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=3, column=3}, end=ChessPosition{row=4, column=3}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnCannotCaptureBackwardWhite(PawnMoveTests.java:380)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            pawnAdvanceBlockedDoubleMoveBlack() ✓
            pawnAdvanceBlockedDoubleMoveWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=2, column=7}, end=ChessPosition{row=3, column=7}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=2, column=7}, end=ChessPosition{row=3, column=7}, promotion=PAWN}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.PawnMoveTests.pawnAdvanceBlockedDoubleMoveWhite(PawnMoveTests.java:175)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

        RookMoveTests (1 passed, 2 failed)
            rookBlocked() ✓
            rookCaptureEnemy() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=3, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=5, column=1}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=3, column=1}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=2}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=4}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=5}, promotion=BISHOP}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.RookMoveTests.rookCaptureEnemy(RookMoveTests.java:35)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            rookMoveUntilEdge() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=1, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=8}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=3, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=4, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=5, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=6, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=7, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=8, column=3}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=1, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=1}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=2}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=4}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=5}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=6}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=7}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=2, column=8}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=3, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=4, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=5, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=6, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=7, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=2, column=3}, end=ChessPosition{row=8, column=3}, promotion=BISHOP}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.RookMoveTests.rookMoveUntilEdge(RookMoveTests.java:12)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

        QueenMoveTests (1 passed, 2 failed)
            queenBlocked() ✓
            queenCaptureEnemy() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=2, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=3, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=3, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=5, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=5, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=6, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=7, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=8, column=1}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=3, column=1}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=2}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=4, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=5, column=1}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=6, column=1}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=7, column=1}, promotion=BISHOP}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.QueenMoveTests.queenCaptureEnemy(QueenMoveTests.java:37)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            queenMoveUntilEdge() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=1, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=1, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=2, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=2, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=3, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=3, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=4, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=4, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=5, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=5, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=6, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=6, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=6, column=8}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=8}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=8, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=8, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=8, column=8}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=1, column=7}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=2, column=7}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=3, column=7}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=4, column=7}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=5, column=7}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=6, column=7}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=1}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=2}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=4}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=5}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=6}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=7, column=8}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=7, column=7}, end=ChessPosition{row=8, column=7}, promotion=BISHOP}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.QueenMoveTests.queenMoveUntilEdge(QueenMoveTests.java:10)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

        BishopMoveTests (1 passed, 2 failed)
            bishopBlocked() ✓
            bishopCaptureEnemy() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=5, column=2}, end=ChessPosition{row=2, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=2}, end=ChessPosition{row=3, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=2}, end=ChessPosition{row=4, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=2}, end=ChessPosition{row=6, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=2}, end=ChessPosition{row=6, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=2}, end=ChessPosition{row=7, column=4}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=5, column=2}, end=ChessPosition{row=3, column=4}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=2}, end=ChessPosition{row=4, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=2}, end=ChessPosition{row=6, column=1}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=2}, end=ChessPosition{row=6, column=3}, promotion=BISHOP}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.BishopMoveTests.bishopCaptureEnemy(BishopMoveTests.java:34)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            bishopMoveUntilEdge() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=1, column=8}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=2, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=2, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=3, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=3, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=4, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=4, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=6, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=6, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=7, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=7, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=8, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=8, column=7}, promotion=null}]> but was: <[ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=1, column=8}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=2, column=1}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=2, column=7}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=3, column=2}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=3, column=6}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=4, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=4, column=5}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=6, column=3}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=6, column=5}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=7, column=2}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=7, column=6}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=8, column=1}, promotion=BISHOP}, ChessMove{start=ChessPosition{row=5, column=4}, end=ChessPosition{row=8, column=7}, promotion=BISHOP}]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.BishopMoveTests.bishopMoveUntilEdge(BishopMoveTests.java:11)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

        KnightMoveTests (0 passed, 13 failed)
            knightBlocked() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=3, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=3, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=4, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=6, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=7, column=6}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightBlocked(KnightMoveTests.java:206)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightCaptureEnemy() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=3, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=3, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=4, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=4, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=6, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=6, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=7, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=7, column=6}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightCaptureEnemy(KnightMoveTests.java:224)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightEdgeOfBoardTop() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=8, column=3}, end=ChessPosition{row=6, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=8, column=3}, end=ChessPosition{row=6, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=8, column=3}, end=ChessPosition{row=7, column=1}, promotion=null}, ChessMove{start=ChessPosition{row=8, column=3}, end=ChessPosition{row=7, column=5}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightEdgeOfBoardTop(KnightMoveTests.java:101)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightEdgeOfBoardLeft() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=2, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=3, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=5, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=4, column=1}, end=ChessPosition{row=6, column=2}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightEdgeOfBoardLeft(KnightMoveTests.java:50)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightEdgeOfBoardRight() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=3, column=8}, end=ChessPosition{row=1, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=8}, end=ChessPosition{row=2, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=8}, end=ChessPosition{row=4, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=3, column=8}, end=ChessPosition{row=5, column=7}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightEdgeOfBoardRight(KnightMoveTests.java:67)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightEdgeOfBoardBottom() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=1, column=6}, end=ChessPosition{row=2, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=1, column=6}, end=ChessPosition{row=2, column=8}, promotion=null}, ChessMove{start=ChessPosition{row=1, column=6}, end=ChessPosition{row=3, column=5}, promotion=null}, ChessMove{start=ChessPosition{row=1, column=6}, end=ChessPosition{row=3, column=7}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightEdgeOfBoardBottom(KnightMoveTests.java:84)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightMiddleOfBoardBlack() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=3, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=3, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=4, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=4, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=6, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=6, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=7, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=7, column=6}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightMiddleOfBoardBlack(KnightMoveTests.java:30)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightMiddleOfBoardWhite() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=3, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=3, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=4, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=4, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=6, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=6, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=7, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=7, column=6}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightMiddleOfBoardWhite(KnightMoveTests.java:11)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightCornerOfBoardTopLeft() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=8, column=1}, end=ChessPosition{row=6, column=2}, promotion=null}, ChessMove{start=ChessPosition{row=8, column=1}, end=ChessPosition{row=7, column=3}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightCornerOfBoardTopLeft(KnightMoveTests.java:153)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightCornerOfBoardTopRight() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=8, column=8}, end=ChessPosition{row=6, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=8, column=8}, end=ChessPosition{row=7, column=6}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightCornerOfBoardTopRight(KnightMoveTests.java:136)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightCornerOfBoardBottomLeft() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=1, column=1}, end=ChessPosition{row=2, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=1, column=1}, end=ChessPosition{row=3, column=2}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightCornerOfBoardBottomLeft(KnightMoveTests.java:170)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightCornerOfBoardBottomRight() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=1, column=8}, end=ChessPosition{row=2, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=1, column=8}, end=ChessPosition{row=3, column=7}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightCornerOfBoardBottomRight(KnightMoveTests.java:119)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

            knightSurroundedButNotBlocked() ✗
             ↳org.opentest4j.AssertionFailedError: Wrong moves ==> expected: <[ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=3, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=3, column=6}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=4, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=4, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=6, column=3}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=6, column=7}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=7, column=4}, promotion=null}, ChessMove{start=ChessPosition{row=5, column=5}, end=ChessPosition{row=7, column=6}, promotion=null}]> but was: <[]>
at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:151)
at org.junit.jupiter.api.AssertionFailureBuilder.buildAndThrow(AssertionFailureBuilder.java:132)
at org.junit.jupiter.api.AssertEquals.failNotEqual(AssertEquals.java:197)
at org.junit.jupiter.api.AssertEquals.assertEquals(AssertEquals.java:182)
at org.junit.jupiter.api.Assertions.assertEquals(Assertions.java:1156)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:32)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:24)
at passoff.chess.TestUtilities.validateMoves(TestUtilities.java:17)
at passoff.chess.piecemoves.KnightMoveTests.knightSurroundedButNotBlocked(KnightMoveTests.java:187)
at java.base/java.lang.reflect.Method.invoke(Method.java:580)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)

    ChessMoveTests (3 passed, 0 failed)
        Equals Testing ✓
        HashCode Testing ✓
        Equals & HashCode Testing ✓
    ChessBoardTests (6 passed, 0 failed)
        Reset Board ✓
        Equals Testing ✓
        HashCode Testing ✓
        Add and Get Piece ✓
        Equals & HashCode Testing ✓
        Construct Empty ChessBoard ✓
    ChessPieceTests (4 passed, 0 failed)
        Equals Testing ✓
        HashCode Testing ✓
        Piece Move on All Pieces ✓
        Equals & HashCode Testing ✓
    ChessPositionTests (3 passed, 0 failed)
