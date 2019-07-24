# vbnet-make-dropdown-
Public Class drop_down_menu

    ' pl1 = panel1 height
    Dim pl1 As Integer = 60

    ' pl2 = panel2 height
    Dim pl2 As Integer = 60

    ' pl3 = panel3 height
    Dim pl3 As Integer = 60

    Private Sub drop_down_menu_Load(sender As Object, e As EventArgs) Handles MyBase.Load


    End Sub

    Private Sub Timer1_Tick(sender As Object, e As EventArgs) Handles Timer1.Tick

        ' 250 = panel height
        If pl1 > 240 Then

            Timer1.Stop()

        Else
            Me.Panel1.Size = New Size(Me.Panel1.Size.Width, pl1)
            pl1 += 10
        End If

    End Sub

    Private Sub Button1_MouseHover(sender As Object, e As EventArgs) Handles Button1.MouseHover

        ' on button1 mouse hover set panel2 and panel3 to the default height (60) 
        Me.Panel2.Size = New Size(Me.Panel2.Size.Width, pl2)
        Me.Panel3.Size = New Size(Me.Panel3.Size.Width, pl3)
        Timer1.Start()

    End Sub

    Private Sub Button1_MouseLeave(sender As Object, e As EventArgs) Handles Button1.MouseLeave

        Timer1.Stop()
        pl1 = 60

    End Sub

    Private Sub Timer2_Tick(sender As Object, e As EventArgs) Handles Timer2.Tick

        If pl2 > 240 Then

            Timer2.Stop()

        Else
            Me.Panel2.Size = New Size(Me.Panel2.Size.Width, pl2)
            pl2 += 10
        End If

    End Sub

    Private Sub Timer3_Tick(sender As Object, e As EventArgs) Handles Timer3.Tick

        If pl3 > 240 Then

            Timer3.Stop()

        Else
            Me.Panel3.Size = New Size(Me.Panel3.Size.Width, pl3)
            pl3 += 10
        End If

    End Sub

    Private Sub Button8_MouseHover(sender As Object, e As EventArgs) Handles Button8.MouseHover

        ' on button8 mouse hover set panel1 and panel3 to the default height (60) 
        Me.Panel1.Size = New Size(Me.Panel1.Size.Width, pl1)
        Me.Panel3.Size = New Size(Me.Panel3.Size.Width, pl3)
        Timer2.Start()

    End Sub

    Private Sub Button8_MouseLeave(sender As Object, e As EventArgs) Handles Button8.MouseLeave

        Timer2.Stop()
        pl2 = 60

    End Sub

    Private Sub Button12_MouseHover(sender As Object, e As EventArgs) Handles Button12.MouseHover

        ' on button12 mouse hover set panel2 and panel1 to the default height (60) 
        Me.Panel2.Size = New Size(Me.Panel2.Size.Width, pl2)
        Me.Panel1.Size = New Size(Me.Panel1.Size.Width, pl1)
        Timer3.Start()

    End Sub

    Private Sub Button12_MouseLeave(sender As Object, e As EventArgs) Handles Button12.MouseLeave

        Timer3.Stop()
        pl3 = 60

    End Sub
End Class

