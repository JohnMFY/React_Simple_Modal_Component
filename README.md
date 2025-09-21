# React_Simple_Modal_Component

A simple customizable solution, easy to use.

## Installation :

    npm install react_simple_modal_component_mfy

## How to use it :

    import React, { useState } from "react";
    import Modal from "react_simple_modal_component_mfy";

    function App() {
    const [isOpen, setIsOpen] = useState(false);

    const openModal = () => setIsOpen(true);
    const closeModal = () => setIsOpen(false);

    return (
        <div>

            <button onClick={openModal}>Open Modal</button>
        
            {isModalOpen && (
                <Modal
                    modalTitle={"modal Title"}
                    modalContent={"modal text content"}
                    closeModal={closeModal}
                    modalBackgroundClass={'modalBackground'}
                    modalClass={'modal'}
                    modalTitleClass={'title'}
                    modalContentClass={'content'}
                    iconClass={'icon'}
                />
            )}

        </div>
    );
    }

    export default App;

## Requirements :

    npm install @fortawesome/fontawesome-free

This component uses Font Awesome for the close icon.

### Props

| Prop                  | Type     |  Required   | Description                                                                 |
|-----------------------|----------|-------------|-----------------------------------------------------------------------------|
| `modalTitle`          | string   | Optional    | Title of the modal.                                                         |
| `modalContent`        | string   | yes         | Text content of the modal .                                                 |
| `closeModal`          | function | yes         | Function to close the modal                                                 |
| `modalBackgroundClass`| string   | Recommended | Class to customize the modal background.                                    |
| `modalClass`          | string   | Recommended | Class to customize the modal.                                               |
| `modalTitleClass`     | string   | no          | Class to customize the modal title (`<h3>`).                                |
| `modalContentClass`   | string   | no          | Class to customize the content of the modal (`<p>`).                        |
| `iconClass`           | string   | Recommended | Class to customize the cross icon used to close the modal onClick.          |
