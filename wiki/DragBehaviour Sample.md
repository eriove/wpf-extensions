# DragBehaviour Sample

Via the DragBehaviour you can modify the position (any kind of position, in the sample below we modify the Canvas.Left, Canvas.Top, but you can bind anything to these properties} of any FrameworkElement or FrameworkContentElement.

{{
<Window ...
    xmlns:extbehaviour="clr-namespace:WPFExtensions.AttachedBehaviours;assembly=WPFExtensions"
    ...>
    <Canvas>
        <Label Content="Hello, I'm Draggable" 
               extbehaviour:DragBehaviour.IsDragEnabled="True" 
               extbehaviour:DragBehaviour.X="{Binding RelativeSource={RelativeSource self},Path=(Canvas.Left),Mode=TwoWay}"
               extbehaviour:DragBehaviour.Y="{Binding RelativeSource={RelativeSource self},Path=(Canvas.Top),Mode=TwoWay}"
               Canvas.Left="0"
               Canvas.Top="50">
        </Label>
        <Label Content="Sorry, I'm not"/>
    </Canvas>
</Window>
}}